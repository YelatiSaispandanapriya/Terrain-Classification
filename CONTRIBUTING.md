# Contributing

Before making any contributions to this repository, please connect with the project owners to discuss proposed changes—whether by opening an issue, sending an email, or using another communication method—prior to submitting modifications.

Remember to review and adhere to our code of conduct in every interaction related to this project.

### Contribution Guidelines

1. **Initiating Contributions**  
   - Always start by submitting an issue before contributing code or suggesting updates.  
   - For fresh ideas, open a separate issue and collaborate with maintainers before moving forward.

2. **Label Usage**  
   - Labels are only assigned once an issue is fully resolved. They will not be used for incomplete work or changes awaiting review.

3. **Adding Models**  
   - For new models created from existing ones with minor tweaks, name them sequentially (e.g., `V1`, `V2`, etc.), reflecting each update. Do **not** overwrite existing files.  
   - Transfer older model files to the `past-architecture` directory to keep track of the progression.  
   - Models using a new method should be named according to that technique, appending the relevant version number (such as `TechniqueName_V1`).

4. **Model Submission Rules**  
   - Every model contributed must include:  
     - A ZIP package of the dataset  
     - The downloaded model file  
     - The model’s achieved accuracy percentage  
   - Each submission should be placed in a dedicated `latest-model` folder showcasing the highest performing model for that method.  
   - **Note:** Only the top-accuracy model should appear outside both the `past-architecture` and `latest-model` folders.

5. **Model Improvements**  
   - If you intend to optimize an existing technique, submit an issue first.  
   - Points or labels are granted only if your updated model achieves better accuracy for that technique. No repeat credit for multiple contributions to the same method.

6. **README Requirement**  
   - New model folders must include a `README.md` describing:  
     - The model’s structure and components  
     - Clear details about its functioning  
   - Ensure that the `README.md` is stored within the model’s folder for accessibility.

7. **Pull Request Standards**  
   - Remove all install/build dependencies before completing the build process.  
   - Update `CHANGES.md` with relevant interface changes—such as new environment variables, ports, file locations, and container configurations.  
   - Revise version numbers in example files and the `README.md` per your pull request.

***

# Code of Conduct

### Our Commitment

As contributors and maintainers, we are dedicated to creating an open, respectful, and harassment-free environment for everyone, regardless of age, appearance, ability, ethnic background, gender identity, experience, nationality, faith, or sexual orientation.

### Community Standards

Behaviors that help sustain a positive experience include:

- Using considerate and inclusive language  
- Appreciating diverse viewpoints and backgrounds  
- Accepting constructive feedback graciously  
- Prioritizing the well-being and interests of the community  
- Demonstrating empathy towards fellow participants

Behaviors considered unacceptable include:

- Making sexualized remarks or sharing inappropriate images  
- Insulting, trolling, or targeting others for personal or political reasons  
- Any form of public or private harassment  
- Posting someone’s private information without permission  
- Conduct deemed unsuitable for a professional community

### Roles and Responsibilities

Maintain project standards by clearly communicating expected behaviors and taking fair action when violations occur.

Project maintainers are authorized to remove, alter, or reject any content or contributions inconsistent with this Code of Conduct, and may restrict access for behaviors considered harmful, threatening, or offensive.

### Coverage

This Code applies not only to official project channels but also whenever individuals act as project representatives in public—whether via official emails, social media, or participation in events. Further details outlining representation may be provided by project maintainers.

### Enforcement Guidelines

We strive for fairness and transparency in handling violations, following these steps:

1. **Warning**  
   A private, written notice will be issued for the first minor offense, clarifying the issue without further action unless behavior repeats.

2. **Temporary Ban**  
   Continued or serious misconduct could lead to a time-limited ban, the length of which reflects the severity and circumstances.

3. **Permanent Ban**  
   Severe, persistent, or intentionally harmful actions may result in permanent expulsion, decided with input from other maintainers.

### Reporting Issues

Anyone may report abuse, harassment, or other unacceptable actions by contacting the project team at [drakathakash@gmail.com](mailto:drakathakash@gmail.com). All inquiries will be investigated and addressed appropriately, with the identity of reporters kept strictly confidential.

Project maintainers who fail to uphold or enforce this code in good faith may also face temporary or permanent disciplinary measures as determined by project leadership.

