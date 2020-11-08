---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F9A06B8B-55DB-48A5-B246-53347E759E64
online version: ''
schema: 2.0.0
ms.openlocfilehash: 050c05f2cdad546388744bcebca4f28a12a03038
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016390"
---
# <span data-ttu-id="f75fa-101">Add-AzurePHPWebRole</span><span class="sxs-lookup"><span data-stu-id="f75fa-101">Add-AzurePHPWebRole</span></span>

## <span data-ttu-id="f75fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f75fa-102">SYNOPSIS</span></span>
<span data-ttu-id="f75fa-103">A PHP-alkalmazások szükséges fájljait és konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="f75fa-103">Creates the required files and configuration for a PHP application.</span></span>

## <span data-ttu-id="f75fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f75fa-104">SYNTAX</span></span>

```
Add-AzurePHPWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f75fa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f75fa-105">DESCRIPTION</span></span>
<span data-ttu-id="f75fa-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="f75fa-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f75fa-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f75fa-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f75fa-108">Az **Add-AzurePHPWebRole** parancsmag az azureon keresztül az IIS-ben üzemelő PHP-alkalmazások számára létrehozza a fájlokat és a konfigurációt (más néven állványzat).</span><span class="sxs-lookup"><span data-stu-id="f75fa-108">The **Add-AzurePHPWebRole** cmdlet creates the files and configuration, sometimes referred to as scaffolding, for a PHP application that will be hosted in Azure through IIS.</span></span>

## <span data-ttu-id="f75fa-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f75fa-109">EXAMPLES</span></span>

### <span data-ttu-id="f75fa-110">1. példa: webes szerepkör felvétele alapértelmezett értékekkel</span><span class="sxs-lookup"><span data-stu-id="f75fa-110">Example 1: Add a web role using default values</span></span>
```
PS C:\> Add-AzurePHPWebRole
```

<span data-ttu-id="f75fa-111">Ebben a példában a "WebRole1" nevű szolgáltatásban 1 példányban szereplő, az új webhelyhez szükséges fájlokat és konfigurációt adja meg.</span><span class="sxs-lookup"><span data-stu-id="f75fa-111">This example adds the required files and configuration for new web role using the default values of a service named "WebRole1" with 1 instance.</span></span>

### <span data-ttu-id="f75fa-112">2. példa: webes szerepkör felvétele több példányban</span><span class="sxs-lookup"><span data-stu-id="f75fa-112">Example 2: Add a web role with multiple instances</span></span>
```
PS C:\> Add-AzurePHPWebRole MyWebRole -I 2
```

<span data-ttu-id="f75fa-113">Ebben a példában a "MyWebRole" nevű új webes szerepkör, a "" és a 2-es számú szerepkör</span><span class="sxs-lookup"><span data-stu-id="f75fa-113">This example adds the required files and configuration for a new web role to the current application, using the name "MyWebRole" and a role instance count of 2.</span></span>

## <span data-ttu-id="f75fa-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f75fa-114">PARAMETERS</span></span>

### <span data-ttu-id="f75fa-115">-Példányok</span><span class="sxs-lookup"><span data-stu-id="f75fa-115">-Instances</span></span>
<span data-ttu-id="f75fa-116">A webes szerepkörhöz tartozó szerepkör-példányok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f75fa-116">Specifies the number of role instances for this web role.</span></span>
<span data-ttu-id="f75fa-117">Az alapértelmezett érték 1.</span><span class="sxs-lookup"><span data-stu-id="f75fa-117">The default is 1.</span></span>

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

### <span data-ttu-id="f75fa-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f75fa-118">-Name</span></span>
<span data-ttu-id="f75fa-119">A webes szerepkör nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f75fa-119">Specifies the name of the web role.</span></span>
<span data-ttu-id="f75fa-120">A név határozza meg annak a könyvtárnak a nevét, amely a PHP alkalmazás szükséges fájljait és konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f75fa-120">The name determines the name of the directory that contains the required files and configuration for the PHP application.</span></span>
<span data-ttu-id="f75fa-121">Az alapértelmezett: webrole #, ahol # a szolgáltatásban elérhető webes szerepkörök száma.</span><span class="sxs-lookup"><span data-stu-id="f75fa-121">The default is WebRole#, where # is the number of web roles in the service.</span></span>

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

### <span data-ttu-id="f75fa-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="f75fa-122">-Profile</span></span>
<span data-ttu-id="f75fa-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="f75fa-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f75fa-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="f75fa-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f75fa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f75fa-125">CommonParameters</span></span>
<span data-ttu-id="f75fa-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f75fa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f75fa-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f75fa-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f75fa-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f75fa-128">INPUTS</span></span>

## <span data-ttu-id="f75fa-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f75fa-129">OUTPUTS</span></span>

## <span data-ttu-id="f75fa-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f75fa-130">NOTES</span></span>

## <span data-ttu-id="f75fa-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f75fa-131">RELATED LINKS</span></span>

[<span data-ttu-id="f75fa-132">Add-AzurePHPWorkerRole</span><span class="sxs-lookup"><span data-stu-id="f75fa-132">Add-AzurePHPWorkerRole</span></span>](./Add-AzurePHPWorkerRole.md)

[<span data-ttu-id="f75fa-133">Új – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="f75fa-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


