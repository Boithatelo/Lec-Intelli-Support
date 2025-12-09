package com.example.demo14;

import javafx.beans.property.*;
import java.util.List;

public class Location {
    private final StringProperty id = new SimpleStringProperty();
    private final StringProperty name = new SimpleStringProperty();
    private final StringProperty description = new SimpleStringProperty();
    private final DoubleProperty xPos = new SimpleDoubleProperty();
    private final DoubleProperty yPos = new SimpleDoubleProperty();
    private final StringProperty audioPath = new SimpleStringProperty();
    private final StringProperty videoPath = new SimpleStringProperty();
    private final ListProperty<QuizQuestion> quizQuestions = new SimpleListProperty<>();

    public Location(String id, String name, String description,
                    double xPos, double yPos,
                    String audioPath, String videoPath,
                    List<QuizQuestion> quizQuestions) {
        setId(id);
        setName(name);
        setDescription(description);
        setXPos(xPos);
        setYPos(yPos);
        setAudioPath(audioPath);
        setVideoPath(videoPath);
        setQuizQuestions(quizQuestions);
    }

    private void setQuizQuestions(List<QuizQuestion> quizQuestions) {
    }

    private void setVideoPath(String videoPath) {
    }

    private void setAudioPath(String audioPath) {
    }

    private void setYPos(double yPos) {
    }

    private void setXPos(double xPos) {
    }

    private void setDescription(String description) {
    }

    // Getters
    public String getId() { return id.get(); }
    public String getName() { return name.get(); }
    public String getDescription() { return description.get(); }
    public double getXPos() { return xPos.get(); }
    public double getYPos() { return yPos.get(); }
    public String getAudioPath() { return audioPath.get(); }
    public String getVideoPath() { return videoPath.get(); }
    public List<QuizQuestion> getQuizQuestions() { return quizQuestions.get(); }

    // Property getters (for JavaFX binding)
    public StringProperty idProperty() { return id; }
    public StringProperty nameProperty() { return name; }
    public StringProperty descriptionProperty() { return description; }
    public DoubleProperty xPosProperty() { return xPos; }
    public DoubleProperty yPosProperty() { return yPos; }
    public StringProperty audioPathProperty() { return audioPath; }
    public StringProperty videoPathProperty() { return videoPath; }
    public ListProperty<QuizQuestion> quizQuestionsProperty() { return quizQuestions; }

    // Setters with validation
    public void setId(String id) {
        if (id == null || id.trim().isEmpty()) {
            throw new IllegalArgumentException("ID cannot be empty");
        }
        this.id.set(id);
    }

    public void setName(String name) {
        if (name == null || name.trim().isEmpty()) {
            throw new IllegalArgumentException("Name cannot be empty");
        }
        this.name.set(name);
    }

    // ... (similar validation for other setters)
}
