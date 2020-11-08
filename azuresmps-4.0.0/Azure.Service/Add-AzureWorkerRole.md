---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8632A865-D4CC-4AE5-8307-055CDD776D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b79ee50bb5097896c2a120a9b7316adb2146b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015710"
---
# <span data-ttu-id="ccc97-101">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="ccc97-101">Add-AzureWorkerRole</span></span>

## <span data-ttu-id="ccc97-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ccc97-102">SYNOPSIS</span></span>
<span data-ttu-id="ccc97-103">Az egyéni munkatársi szerepkör szükséges fájljait és konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="ccc97-103">Creates required files and configuration for a custom worker role.</span></span>

## <span data-ttu-id="ccc97-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ccc97-104">SYNTAX</span></span>

```
Add-AzureWorkerRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ccc97-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ccc97-105">DESCRIPTION</span></span>
<span data-ttu-id="ccc97-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="ccc97-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ccc97-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ccc97-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ccc97-108">A **Add-AzureWorkerRole** parancsmag szükséges fájlokat és konfigurációt hoz létre, olykor állványzat néven, egyéni munkatársi szerepkör esetén.</span><span class="sxs-lookup"><span data-stu-id="ccc97-108">The **Add-AzureWorkerRole** cmdlet creates required files and configuration, sometimes referred to as scaffolding, for a custom worker role.</span></span>

## <span data-ttu-id="ccc97-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ccc97-109">EXAMPLES</span></span>

### <span data-ttu-id="ccc97-110">1. példa: egypéldányos munkatársi szerepkör létrehozása</span><span class="sxs-lookup"><span data-stu-id="ccc97-110">Example 1: Create a single instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole -Name MyWorkerRole
```

<span data-ttu-id="ccc97-111">Ez a példa összeadja az állványzatot egyetlen, a MyWorkerRole nevű, a jelenlegi alkalmazáshoz tartozó szerepkörnek.</span><span class="sxs-lookup"><span data-stu-id="ccc97-111">This example adds scaffolding for a single worker role named MyWorkerRole to the current application.</span></span>

### <span data-ttu-id="ccc97-112">2. példa: több példányos munkatársi szerepkör létrehozása</span><span class="sxs-lookup"><span data-stu-id="ccc97-112">Example 2: Create a multiple instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="ccc97-113">Ez a példa összeadja az állványzatot egy új, MyWorkerRole nevű munkatársi szerepkörhez, amelynek a szerepkör-példánya 2.</span><span class="sxs-lookup"><span data-stu-id="ccc97-113">This example adds scaffolding for a new worker role named MyWorkerRole to the current application, with a role instance count of 2.</span></span>

### <span data-ttu-id="ccc97-114">3. példa: a munkatársi szerepkör létrehozása egyéni állványzattal</span><span class="sxs-lookup"><span data-stu-id="ccc97-114">Example 3: Create worker role with custom scaffolding</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -TemplateFoldr .\MyWorkerRoleTemplate
```

<span data-ttu-id="ccc97-115">Ez a példa létrehoz egy munkatársi szerepkört az egyéni állványzattal.</span><span class="sxs-lookup"><span data-stu-id="ccc97-115">This example creates a worker role with custom scaffolding.</span></span>

## <span data-ttu-id="ccc97-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ccc97-116">PARAMETERS</span></span>

### <span data-ttu-id="ccc97-117">-Példányok</span><span class="sxs-lookup"><span data-stu-id="ccc97-117">-Instances</span></span>
<span data-ttu-id="ccc97-118">A munkatársi szerepkörhöz tartozó szerepkör-példányok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ccc97-118">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="ccc97-119">Az alapértelmezett érték 1.</span><span class="sxs-lookup"><span data-stu-id="ccc97-119">The default is 1.</span></span>

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

### <span data-ttu-id="ccc97-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ccc97-120">-Name</span></span>
<span data-ttu-id="ccc97-121">A munkatársi szerepkör nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ccc97-121">Specifies the name of the worker role.</span></span>
<span data-ttu-id="ccc97-122">Ez az érték határozza meg azt a mappát, amely a munkatársi szerepkörben üzemeltetni kívánt egyéni alkalmazás állványzatát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ccc97-122">This value determines the folder name that contains the scaffolding for the custom application that will be hosted in the worker role.</span></span>
<span data-ttu-id="ccc97-123">Az alapértelmezett érték a WorkerRolenumber, ahol a szám a szolgáltatásban alkalmazott szerepkörök száma.</span><span class="sxs-lookup"><span data-stu-id="ccc97-123">The default is WorkerRolenumber, where number is the number of worker roles in the service.</span></span>

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

### <span data-ttu-id="ccc97-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="ccc97-124">-Profile</span></span>
<span data-ttu-id="ccc97-125">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ccc97-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ccc97-126">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ccc97-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ccc97-127">-TemplateFolder</span><span class="sxs-lookup"><span data-stu-id="ccc97-127">-TemplateFolder</span></span>
<span data-ttu-id="ccc97-128">A munkatársi szerepkör létrehozásához használandó állványzat sablon mappáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ccc97-128">Specifies the scaffolding template folder to be used to create the worker role.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccc97-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccc97-129">CommonParameters</span></span>
<span data-ttu-id="ccc97-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ccc97-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccc97-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccc97-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccc97-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccc97-132">INPUTS</span></span>

## <span data-ttu-id="ccc97-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccc97-133">OUTPUTS</span></span>

## <span data-ttu-id="ccc97-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ccc97-134">NOTES</span></span>

## <span data-ttu-id="ccc97-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ccc97-135">RELATED LINKS</span></span>

[<span data-ttu-id="ccc97-136">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="ccc97-136">Add-AzureWebRole</span></span>](./Add-AzureWebRole.md)

[<span data-ttu-id="ccc97-137">Új – AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="ccc97-137">New-AzureRoleTemplate</span></span>](./New-AzureRoleTemplate.md)


