# ============================================================================
# Makefile for Professional Sudoku Solver System
# ============================================================================

# Compiler and flags
CXX := g++
CXXFLAGS := -std=c++17 -Wall -Wextra -Wpedantic -Werror -O2
LDFLAGS := 

# Source files
SRCS := main.cpp Sudoku.cpp FileManager.cpp
OBJS := $(SRCS:.cpp=.o)
TARGET := SudokuSolver

# SFML GUI (optional)
GUI_SRCS := gui.cpp
GUI_TARGET := SudokuSolverGUI
GUI_LDFLAGS := -lsfml-graphics -lsfml-window -lsfml-system

# ============================================================================
# Colors for output
# ============================================================================
GREEN := \033[32m
CYAN := \033[36m
YELLOW := \033[33m
RESET := \033[0m

# ============================================================================
# Targets
# ============================================================================

all: $(TARGET)
	@echo "$(GREEN)✓ Build complete! Run: ./$(TARGET)$(RESET)"

$(TARGET): $(OBJS)
	@echo "$(CYAN)Linking...$(RESET)"
	$(CXX) $(CXXFLAGS) -o $@ $^ $(LDFLAGS)
	@echo "$(GREEN)✓ Successfully built $(TARGET)$(RESET)"

%.o: %.cpp
	@echo "$(CYAN)Compiling $<...$(RESET)"
	$(CXX) $(CXXFLAGS) -c $< -o $@

# GUI target (conditional - requires SFML)
gui: $(GUI_TARGET)
	@echo "$(GREEN)✓ GUI build complete! Run: ./$(GUI_TARGET)$(RESET)"

$(GUI_TARGET): $(OBJS) gui.o
	@echo "$(CYAN)Linking GUI...$(RESET)"
	$(CXX) $(CXXFLAGS) -o $@ $^ $(GUI_LDFLAGS)
	@echo "$(GREEN)✓ Successfully built $(GUI_TARGET)$(RESET)"

# Clean build artifacts
clean:
	@echo "$(YELLOW)Cleaning...$(RESET)"
	rm -f $(OBJS) gui.o $(TARGET) $(GUI_TARGET)
	@echo "$(GREEN)✓ Clean complete$(RESET)"

# Rebuild everything
rebuild: clean all

# Run the application
run: $(TARGET)
	@echo "$(CYAN)Running $(TARGET)...$(RESET)"
	./$(TARGET)

# Run with GUI
rungui: $(GUI_TARGET)
	@echo "$(CYAN)Running $(GUI_TARGET)...$(RESET)"
	./$(GUI_TARGET)

# Install dependencies (macOS)
install-macos:
	@echo "$(YELLOW)Installing dependencies for macOS...$(RESET)"
	brew install gcc sfml || true
	@echo "$(GREEN)✓ Installation complete$(RESET)"

# Install dependencies (Ubuntu/Debian)
install-linux:
	@echo "$(YELLOW)Installing dependencies for Linux...$(RESET)"
	sudo apt update
	sudo apt install -y g++ make libsfml-dev
	@echo "$(GREEN)✓ Installation complete$(RESET)"

# Format code (requires clang-format)
format:
	@echo "$(YELLOW)Formatting code...$(RESET)"
	clang-format -i *.cpp *.h || true
	@echo "$(GREEN)✓ Format complete$(RESET)"

# Count lines of code
loc:
	@echo "$(CYAN)Lines of code:$(RESET)"
	@wc -l *.cpp *.h *.md 2>/dev/null | tail -1

# Create necessary directories
dirs:
	mkdir -p screenshots docs assets

# Help
help:
	@echo "$(CYAN)Available targets:$(RESET)"
	@echo "  all        - Build console application (default)"
	@echo "  gui        - Build with GUI support (requires SFML)"
	@echo "  run        - Run console application"
	@echo "  rungui     - Run GUI application"
	@echo "  clean      - Remove build artifacts"
	@echo "  rebuild    - Clean and rebuild"
	@echo "  format     - Format source code"
	@echo "  loc        - Count lines of code"
	@echo "  dirs       - Create necessary directories"
	@echo "  help       - Show this help"

.PHONY: all gui clean rebuild run rungui format loc dirs help install-macos install-linux

