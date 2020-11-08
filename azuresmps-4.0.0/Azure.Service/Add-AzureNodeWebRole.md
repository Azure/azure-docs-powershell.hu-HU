---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C2DAFB2C-A58B-406C-8349-8728771B279E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59aef29c27d7eb96834d270c2fce48ff3acb9554
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016392"
---
# <span data-ttu-id="4a8e2-101">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="4a8e2-101">Add-AzureNodeWebRole</span></span>

## <span data-ttu-id="4a8e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4a8e2-102">SYNOPSIS</span></span>
<span data-ttu-id="4a8e2-103">A Node.js-alkalmazások szükséges fájljait és mappáit hozza létre.</span><span class="sxs-lookup"><span data-stu-id="4a8e2-103">Creates required files and folders for a Node.js application.</span></span>

## <span data-ttu-id="4a8e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4a8e2-104">SYNTAX</span></span>

```
Add-AzureNodeWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4a8e2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4a8e2-105">DESCRIPTION</span></span>
<span data-ttu-id="4a8e2-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="4a8e2-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4a8e2-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="4a8e2-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="4a8e2-108">Az **Add-AzureNodeWebRole** létrehozza a szükséges fájlokat és mappákat, amelyeket néha állványzatnak is neveznek, ha egy Node.js alkalmazást a felhőbe az IIS-en keresztül tárol.</span><span class="sxs-lookup"><span data-stu-id="4a8e2-108">The **Add-AzureNodeWebRole** creates required files and folders, sometimes referred to as scaffolding, for a Node.js application to be hosted in the cloud via IIS.</span></span>

## <span data-ttu-id="4a8e2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4a8e2-109">EXAMPLES</span></span>

### <span data-ttu-id="4a8e2-110">Példa 1: Single instance web role</span><span class="sxs-lookup"><span data-stu-id="4a8e2-110">Example 1: Single instance web role</span></span>
```
PS C:\> Add-AzureNodeWebRole -Name MyWebRole
```

<span data-ttu-id="4a8e2-111">Ez a példa összeadja az állványzatot az **MyWebRole** nevű webszerephez az aktuális alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="4a8e2-111">This example adds scaffolding for a single web role named **MyWebRole** to the current application.</span></span>

### <span data-ttu-id="4a8e2-112">2. példa: több példányos webszerepkör</span><span class="sxs-lookup"><span data-stu-id="4a8e2-112">Example 2: Multiple instance web role</span></span>
```
PS C:\> Add-AzureNodeWebRole MyWebRole -I 2
```

<span data-ttu-id="4a8e2-113">Ez a példa összeadja az állványzatot a **MyWebRole** nevű új webszerephez, amelynek a szerepkör-példánya 2.</span><span class="sxs-lookup"><span data-stu-id="4a8e2-113">This example adds scaffolding for a new web role named **MyWebRole** to the current application, with a role instance count of 2.</span></span>

## <span data-ttu-id="4a8e2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4a8e2-114">PARAMETERS</span></span>

### <span data-ttu-id="4a8e2-115">-Példányok</span><span class="sxs-lookup"><span data-stu-id="4a8e2-115">-Instances</span></span>
<span data-ttu-id="4a8e2-116">A webes szerepkörhöz tartozó szerepkör-példányok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a8e2-116">Specifies the number of role instances for this web role.</span></span>
<span data-ttu-id="4a8e2-117">Az alapértelmezett érték 1.</span><span class="sxs-lookup"><span data-stu-id="4a8e2-117">The default is 1.</span></span>

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

### <span data-ttu-id="4a8e2-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4a8e2-118">-Name</span></span>
<span data-ttu-id="4a8e2-119">A webes szerepkör nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a8e2-119">Specifies the name of the web role.</span></span>
<span data-ttu-id="4a8e2-120">Annak a könyvtárnak a nevét adja meg, amely a webes szerepkörben üzemeltetni kívánt node.js-alkalmazás állványzatát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4a8e2-120">It also determines the name of the directory that contains the scaffolding for the node.js application that will be hosted in the web role.</span></span>
<span data-ttu-id="4a8e2-121">Az alapértelmezett: webrole #, ahol a # a szolgáltatásban a webes szerepkörök számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4a8e2-121">The default is WebRole#, where # indicates the number of web roles in the service.</span></span>

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

### <span data-ttu-id="4a8e2-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="4a8e2-122">-Profile</span></span>
<span data-ttu-id="4a8e2-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="4a8e2-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4a8e2-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="4a8e2-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4a8e2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a8e2-125">CommonParameters</span></span>
<span data-ttu-id="4a8e2-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4a8e2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a8e2-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a8e2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a8e2-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a8e2-128">INPUTS</span></span>

## <span data-ttu-id="4a8e2-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a8e2-129">OUTPUTS</span></span>

## <span data-ttu-id="4a8e2-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4a8e2-130">NOTES</span></span>

## <span data-ttu-id="4a8e2-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a8e2-131">RELATED LINKS</span></span>

[<span data-ttu-id="4a8e2-132">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="4a8e2-132">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="4a8e2-133">Új – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="4a8e2-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


