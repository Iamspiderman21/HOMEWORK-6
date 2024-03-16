# HOMEWORK-6

// database/seeds/UsuariosSeeder.php
use Illuminate\Database\Seeder;
use App\User;

class UsuariosSeeder extends Seeder
{
    public function run()
    {
        User::create([
            'name' => 'Admon',
            'email' => 'admon@robotics.com',
            'password' => bcrypt('Adm@2022'),
            'role' => 'Administrativo',
        ]);

        User::create([
            'name' => 'Tecmilenio',
            'email' => 'tecmilenio@robotics.com',
            'password' => bcrypt('Adm@2022'),
            'role' => 'Docente',
        ]);

        User::create([
            'name' => 'Estudiante',
            'email' => 'estudiante@robotics.com',
            'password' => bcrypt('Adm@2022'),
            'role' => 'Estudiante',
        ]);
    }
}

// database/seeds/KitsSeeder.php
use Illuminate\Database\Seeder;
use App\Kit;

class KitsSeeder extends Seeder
{
    public function run()
    {
        // Suponiendo que Kit es un modelo
        Kit::create([
            'nombre' => 'Kit A',
            'descripcion' => 'Descripción del Kit A',
            // Otros campos del Kit A
        ]);

        Kit::create([
            'nombre' => 'Kit B',
            'descripcion' => 'Descripción del Kit B',
            // Otros campos del Kit B
        ]);

        Kit::create([
            'nombre' => 'Kit C',
            'descripcion' => 'Descripción del Kit C',
            // Otros campos del Kit C
        ]);
    }
}

// database/factories/CursoFactory.php
use Faker\Generator as Faker;
use App\Curso;

$factory->define(Curso::class, function (Faker $faker) {
    return [
        'nombre' => $faker->sentence,
        'descripcion' => $faker->paragraph,
        // Otros campos del curso
    ];
});
