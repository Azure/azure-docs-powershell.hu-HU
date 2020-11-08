---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E499868E-A745-4CA4-A717-C33C3B94A2C8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b80071bb82ebbb960be5b5b4fcc854dc47c9ed9d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015992"
---
# <span data-ttu-id="9e0d3-101">New-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="9e0d3-101">New-AzureRoleTemplate</span></span>

## <span data-ttu-id="9e0d3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e0d3-102">SYNOPSIS</span></span>
<span data-ttu-id="9e0d3-103">A web-és a munkatársi szerepkör-sablonok létrehozása.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-103">Creates web and worker role templates.</span></span>

## <span data-ttu-id="9e0d3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e0d3-104">SYNTAX</span></span>

### <span data-ttu-id="9e0d3-105">Webszerepkör</span><span class="sxs-lookup"><span data-stu-id="9e0d3-105">WebRole</span></span>
```
New-AzureRoleTemplate [-Web] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9e0d3-106">WorkerRole</span><span class="sxs-lookup"><span data-stu-id="9e0d3-106">WorkerRole</span></span>
```
New-AzureRoleTemplate [-Worker] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9e0d3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e0d3-107">DESCRIPTION</span></span>
<span data-ttu-id="9e0d3-108">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9e0d3-109">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9e0d3-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9e0d3-110">A **New-AzureRoleTemplate** parancsmag a webes és a munkavégző szerepkör-sablonokat hozza létre.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-110">The **New-AzureRoleTemplate** cmdlet creates web and worker role templates.</span></span>

## <span data-ttu-id="9e0d3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9e0d3-111">EXAMPLES</span></span>

### <span data-ttu-id="9e0d3-112">1. példa: webszerepkör-sablon létrehozása</span><span class="sxs-lookup"><span data-stu-id="9e0d3-112">Example 1: Create a web role template</span></span>
```
PS C:\> New-AzureRoleTemplate -Web
```

<span data-ttu-id="9e0d3-113">Ez a példa új webszerepkör-sablont hoz létre az aktuális könyvtár WebRoleTemplate nevű mappájában.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-113">This example creates a new web role template in a folder named WebRoleTemplate in the current directory.</span></span>

### <span data-ttu-id="9e0d3-114">2. példa: munkatársi szerepkörű sablon létrehozása</span><span class="sxs-lookup"><span data-stu-id="9e0d3-114">Example 2: Create a worker role template</span></span>
```
PS C:\> New-AzureRoleTemplate -Worker
```

<span data-ttu-id="9e0d3-115">Ez a példa létrehoz egy új munkatársi szerepkör-sablont az aktuális könyvtár WebRoleTemplate nevű mappájában.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-115">This example creates a new worker role template in a folder named WebRoleTemplate in the current directory.</span></span>

### <span data-ttu-id="9e0d3-116">3. példa: szerepkör-sablon létrehozása egyéni címtárban</span><span class="sxs-lookup"><span data-stu-id="9e0d3-116">Example 3: Create a role template in a custom directory</span></span>
```
PS C:\> New-AzureRoleTemplate -Web -Output C:\MyWebRoleTemplate
```

<span data-ttu-id="9e0d3-117">Ez a példa új webszerepkör-sablont hoz létre a MyWebRoleTemplate nevű címtárban az aktuális könyvtár helyett.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-117">This example creates a new web role template in directory named MyWebRoleTemplate, instead of in the current directory.</span></span>

## <span data-ttu-id="9e0d3-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e0d3-118">PARAMETERS</span></span>

### <span data-ttu-id="9e0d3-119">-Output (kimenet)</span><span class="sxs-lookup"><span data-stu-id="9e0d3-119">-Output</span></span>
<span data-ttu-id="9e0d3-120">A generált sablon kimeneti elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-120">Specifies the output path of generated template.</span></span>

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

### <span data-ttu-id="9e0d3-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="9e0d3-121">-Profile</span></span>
<span data-ttu-id="9e0d3-122">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9e0d3-123">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9e0d3-124">– Webes</span><span class="sxs-lookup"><span data-stu-id="9e0d3-124">-Web</span></span>
<span data-ttu-id="9e0d3-125">Azt adja meg, hogy webszerepkör-sablont szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-125">Specifies that you want to create a web role template.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e0d3-126">-Munkás</span><span class="sxs-lookup"><span data-stu-id="9e0d3-126">-Worker</span></span>
<span data-ttu-id="9e0d3-127">Itt adhatja meg, hogy egy munkatársi szerepkör-sablont szeretne létrehozni.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-127">Specifies that you want to create a worker role template.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WorkerRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e0d3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e0d3-128">CommonParameters</span></span>
<span data-ttu-id="9e0d3-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e0d3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e0d3-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e0d3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e0d3-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e0d3-131">INPUTS</span></span>

## <span data-ttu-id="9e0d3-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e0d3-132">OUTPUTS</span></span>

## <span data-ttu-id="9e0d3-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e0d3-133">NOTES</span></span>

## <span data-ttu-id="9e0d3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e0d3-134">RELATED LINKS</span></span>

[<span data-ttu-id="9e0d3-135">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="9e0d3-135">Add-AzureWebRole</span></span>](./Add-AzureWebRole.md)

[<span data-ttu-id="9e0d3-136">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="9e0d3-136">Add-AzureWorkerRole</span></span>](./Add-AzureWorkerRole.md)


