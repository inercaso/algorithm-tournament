# Pattern Recognition Avenger

A sophisticated strategy for the Prisoner's Dilemma tournament that combines pattern recognition, trust-based decision making, and adaptive responses to opponent behavior.

## Strategy Overview

The Pattern Recognition Avenger is designed to:
- Recognize and exploit repeating patterns in opponent behavior
- Build and maintain trust with cooperative opponents
- Retaliate against defectors while allowing for forgiveness
- Adapt its strategy based on game length and opponent behavior

## Key Features

### 1. Pattern Recognition
- Analyzes opponent's recent moves to detect repeating patterns
- Uses pattern prediction to anticipate opponent's next move
- Limited to last 3 moves for efficiency

### 2. Trust-Based Decision Making
- Maintains a dynamic trust score (0.0 to 1.0)
- Recent moves have more impact on trust calculation
- Trust increases with cooperation, decreases with defection
- Limited to last 20 moves for performance

### 3. Adaptive Response Patterns
- Tracks how opponents respond to cooperation and defection
- Identifies consistent response patterns
- Exploits predictable opponent behavior
- Limited to last 10 moves for analysis

### 4. Strategic Decision Making
- Starts cooperatively in long games (>50 rounds)
- Starts defensively in short games
- Defects in final rounds when game length is known
- Retaliates against highly aggressive opponents (>70% defection rate)

### 5. Performance Optimizations
- Efficient memory usage through history limits
- Fast execution time through optimized pattern matching
- No external dependencies
- Clean, maintainable code structure

## Decision Process

1. **First Move**
    - Cooperate if game is long (>50 rounds)
    - Defect if game is short or length unknown

2. **Pattern Recognition**
    - Look for repeating patterns in opponent's moves
    - Predict next move based on pattern history

3. **Trust Evaluation**
    - Calculate trust score based on opponent's history
    - Weight recent moves more heavily

4. **Response Analysis**
    - Track opponent's responses to cooperation/defection
    - Identify consistent response patterns

5. **Final Decision**
    - Consider game length and remaining rounds
    - Evaluate opponent's aggression level
    - Apply pattern recognition results
    - Use trust score for forgiveness/retaliation
    - Make final move based on all factors

## Technical Details

- **Function Signature**: `strategy(my_history: list[int], opponent_history: list[int], rounds: int | None) -> int`
- **Return Values**:
    - `1` for cooperation
    - `0` for defection
- **Memory Usage**: Optimized to stay within 50MB
- **Execution Time**: Optimized to stay under 200ms per call

## Strategy Philosophy

The Pattern Recognition Avenger aims to:
- Build mutually beneficial relationships with cooperative opponents
- Protect itself from exploitation by defectors
- Adapt to different opponent strategies
- Maintain high performance in both short and long games
- Balance between cooperation and self-protection 