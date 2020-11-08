---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7190C668-6A0C-4E1D-9B5A-0CEEF53E3F85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93573caf43a6c711e1aa1308c851c82faaef5bcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016389"
---
# <span data-ttu-id="5a407-101">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="5a407-101">Add-AzureNodeWorkerRole</span></span>

## <span data-ttu-id="5a407-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a407-102">SYNOPSIS</span></span>
<span data-ttu-id="5a407-103">Létrehozza a Node.js-alkalmazás szükséges fájljait és mappáit a felhőn keresztül node.exe</span><span class="sxs-lookup"><span data-stu-id="5a407-103">Creates the required files and folders for a Node.js application to be hosted in the cloud via node.exe</span></span>

## <span data-ttu-id="5a407-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a407-104">SYNTAX</span></span>

```
Add-AzureNodeWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5a407-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a407-105">DESCRIPTION</span></span>
<span data-ttu-id="5a407-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="5a407-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5a407-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="5a407-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5a407-108">A **Add-AzureNodeWorkerRole** parancsmag létrehozza a szükséges fájlokat és mappákat, amelyeket időnként az állványzatnak is nevezünk, mert egy Node.js alkalmazás a felhőn keresztül node.exeen tárol.</span><span class="sxs-lookup"><span data-stu-id="5a407-108">The **Add-AzureNodeWorkerRole** cmdlet creates the required files and folders, sometimes referred to as scaffolding, for a Node.js application to be hosted in the cloud via node.exe.</span></span>

## <span data-ttu-id="5a407-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5a407-109">EXAMPLES</span></span>

### <span data-ttu-id="5a407-110">Példa 1: egypéldányos munkatársi szerepkör</span><span class="sxs-lookup"><span data-stu-id="5a407-110">Example 1: Single instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole
```

<span data-ttu-id="5a407-111">Ez a példa összeadja az állványzatot egyetlen, a **MyWorkerRole** nevű, a jelenlegi alkalmazáshoz tartozó szerepkörnek.</span><span class="sxs-lookup"><span data-stu-id="5a407-111">This example adds scaffolding for a single worker role named **MyWorkerRole** to the current application.</span></span>

### <span data-ttu-id="5a407-112">2. példa: több példányos munkatárs szerepkör</span><span class="sxs-lookup"><span data-stu-id="5a407-112">Example 2: Multiple instance worker role</span></span>
```
PS C:\> Add-AzureNodeWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="5a407-113">Ez a példa összeadja az állványzatot egy, a **MyWorkerRole** nevű, a jelenlegi alkalmazáshoz nevű egyetlen munkatársi szerepkörnek, amelynek a szerepkör-példánya 2.</span><span class="sxs-lookup"><span data-stu-id="5a407-113">This example adds scaffolding for a single worker role named **MyWorkerRole** to the current application, with a role instance count of 2.</span></span>

## <span data-ttu-id="5a407-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a407-114">PARAMETERS</span></span>

### <span data-ttu-id="5a407-115">-Példányok</span><span class="sxs-lookup"><span data-stu-id="5a407-115">-Instances</span></span>
<span data-ttu-id="5a407-116">A munkatársi szerepkörhöz tartozó szerepkör-példányok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a407-116">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="5a407-117">Az alapértelmezett érték 1.</span><span class="sxs-lookup"><span data-stu-id="5a407-117">Default is 1.</span></span>

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

### <span data-ttu-id="5a407-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5a407-118">-Name</span></span>
<span data-ttu-id="5a407-119">A munkatársi szerepkör nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a407-119">Specifies the name of the worker role.</span></span>
<span data-ttu-id="5a407-120">Az érték határozza meg a munkatársi szerepkörben szereplő node.js-szolgáltatás állványzatát tartalmazó mappa nevét.</span><span class="sxs-lookup"><span data-stu-id="5a407-120">The value determines the folder name that contains the scaffolding for the node.js service hosted in the worker role.</span></span>
<span data-ttu-id="5a407-121">Az alapértelmezett érték a WorkerRole1.</span><span class="sxs-lookup"><span data-stu-id="5a407-121">Default is WorkerRole1.</span></span>

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

### <span data-ttu-id="5a407-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="5a407-122">-Profile</span></span>
<span data-ttu-id="5a407-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="5a407-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5a407-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="5a407-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5a407-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a407-125">CommonParameters</span></span>
<span data-ttu-id="5a407-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a407-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a407-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a407-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a407-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a407-128">INPUTS</span></span>

## <span data-ttu-id="5a407-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a407-129">OUTPUTS</span></span>

## <span data-ttu-id="5a407-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a407-130">NOTES</span></span>

## <span data-ttu-id="5a407-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a407-131">RELATED LINKS</span></span>

[<span data-ttu-id="5a407-132">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="5a407-132">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="5a407-133">Új – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="5a407-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


