<a href="https://wakatime.com/@018cc8f5-2dde-4e5c-b91c-53407ae38aa2"><img src="https://wakatime.com/badge/user/018cc8f5-2dde-4e5c-b91c-53407ae38aa2.svg" alt="Total time coded since Jan 2 2024" /></a>

```go
type sambok struct {
	Name                  string
	GitHub                string
	Email                 string
	TechStack             []string
	EngineeringPhilosophy []string
	Education             []string
	Career                []string
	Community             []string
}

func (s *sambok) NewSambok() *sambok {
	return &sambok{
		Name:   "Hyunseo Jung",
		GitHub: "3boku",
		Email:  "a24746440@gmail.com",
		TechStack: []string{
			"Go", "TypeScript",
		},
		EngineeringPhilosophy: []string{
			"Ship fast, iterate faster",
			"Automation over repetition",
			"Product > Code",
		},
		Education: []string{
			"Seoul Robotics HighSchool Graduate",
			"Hanyang Cyber University Department of Computer Science and Engineering",
		},
		Career: []string{
			"ex. Clika Inc. Software Engineer Intern",
			"PostMath Software Engineer",
		},
		Community: []string{
			"ex. KSDC Lead Organizer",
			"GDG Golang Korea Organizer",
		},
	}
}
```
