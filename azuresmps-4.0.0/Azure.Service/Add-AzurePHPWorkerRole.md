---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FEFBF1EF-FBCE-45D8-8455-F3F8662F1F36
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ddf78f30cb6938571fc967d510e4ab99a0cfc80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016387"
---
# <span data-ttu-id="6aa2d-101">Add-AzurePHPWorkerRole</span><span class="sxs-lookup"><span data-stu-id="6aa2d-101">Add-AzurePHPWorkerRole</span></span>

## <span data-ttu-id="6aa2d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6aa2d-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa2d-103">Létrehozza a szükséges fájlokat és konfigurációt egy olyan PHP-alkalmazáshoz, amelyet az Azure-on php.exe-ben fog üzemeltetni.</span><span class="sxs-lookup"><span data-stu-id="6aa2d-103">Creates the required files and configuration for a PHP application that will be hosted in Azure through php.exe.</span></span>

## <span data-ttu-id="6aa2d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6aa2d-104">SYNTAX</span></span>

```
Add-AzurePHPWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6aa2d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6aa2d-105">DESCRIPTION</span></span>
<span data-ttu-id="6aa2d-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="6aa2d-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6aa2d-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6aa2d-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6aa2d-108">A szükséges fájlokat és konfigurációt hozza létre (más néven állványzat) egy olyan PHP-alkalmazáshoz, amelyet az Azure-ban php.exe-ban fog üzemeltetni.</span><span class="sxs-lookup"><span data-stu-id="6aa2d-108">Creates the required files and configuration, sometimes referred to as scaffolding, for a PHP application that will be hosted in Azure through php.exe.</span></span>

## <span data-ttu-id="6aa2d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6aa2d-109">EXAMPLES</span></span>

### <span data-ttu-id="6aa2d-110">1. példa: a munkatársi szerepkör létrehozása egyetlen példánnyal</span><span class="sxs-lookup"><span data-stu-id="6aa2d-110">Example 1: Create a worker role with a single instance</span></span>
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole
```

<span data-ttu-id="6aa2d-111">Ebben a példában a MyWorkerRole az aktuális alkalmazáshoz nevű egyetlen alkalmazotti szerepkör szükséges fájljait és konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6aa2d-111">This example adds the required files and configuration for a single worker role named MyWorkerRole to the current application.</span></span>

### <span data-ttu-id="6aa2d-112">2. példa: munkatársi szerepkör létrehozása több példányban</span><span class="sxs-lookup"><span data-stu-id="6aa2d-112">Example 2: Create a worker role with multiple instances</span></span>
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="6aa2d-113">Ez a példa összeadja az új munkatársi szerepkör szükséges fájljait és konfigurációját a jelenlegi alkalmazáshoz, és a MyWorkerRole nevet használja, és a szerepkör-példányok száma 2.</span><span class="sxs-lookup"><span data-stu-id="6aa2d-113">This example adds the required files and configuration for a new worker role to the current application, using the name MyWorkerRole with a role instance count of 2.</span></span>

## <span data-ttu-id="6aa2d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6aa2d-114">PARAMETERS</span></span>

### <span data-ttu-id="6aa2d-115">-Példányok</span><span class="sxs-lookup"><span data-stu-id="6aa2d-115">-Instances</span></span>
<span data-ttu-id="6aa2d-116">A munkatársi szerepkörhöz tartozó szerepkör-példányok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6aa2d-116">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="6aa2d-117">Az alapértelmezett érték 1.</span><span class="sxs-lookup"><span data-stu-id="6aa2d-117">The default is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aa2d-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6aa2d-118">-Name</span></span>
<span data-ttu-id="6aa2d-119">A munkatársi szerepkör nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6aa2d-119">Specifies the name of the worker role.</span></span>
<span data-ttu-id="6aa2d-120">A név határozza meg azt a mappát, amely a munkatársi szerepkörben található PHP szolgáltatás szükséges fájljait és konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6aa2d-120">The name determines the folder name that contains the required files and configuration for the PHP service hosted in the worker role.</span></span>
<span data-ttu-id="6aa2d-121">Az alapértelmezett érték a WorkerRole1.</span><span class="sxs-lookup"><span data-stu-id="6aa2d-121">The default is WorkerRole1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aa2d-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="6aa2d-122">-Profile</span></span>
<span data-ttu-id="6aa2d-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="6aa2d-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6aa2d-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="6aa2d-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aa2d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa2d-125">CommonParameters</span></span>
<span data-ttu-id="6aa2d-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6aa2d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa2d-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aa2d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa2d-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6aa2d-128">INPUTS</span></span>

## <span data-ttu-id="6aa2d-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6aa2d-129">OUTPUTS</span></span>

## <span data-ttu-id="6aa2d-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6aa2d-130">NOTES</span></span>

## <span data-ttu-id="6aa2d-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6aa2d-131">RELATED LINKS</span></span>

[<span data-ttu-id="6aa2d-132">Új – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="6aa2d-132">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="6aa2d-133">Add-AzurePHPWebRole</span><span class="sxs-lookup"><span data-stu-id="6aa2d-133">Add-AzurePHPWebRole</span></span>](./Add-AzurePHPWebRole.md)


