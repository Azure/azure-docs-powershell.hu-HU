---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 815b8a7feb22e754302c455c7666f8408c348c92
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467966"
---
# <span data-ttu-id="fbbe8-101">New-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fbbe8-101">New-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="fbbe8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbbe8-102">SYNOPSIS</span></span>
<span data-ttu-id="fbbe8-103">Létrehoz egy új Edge Storage-fiókot az eszközön.</span><span class="sxs-lookup"><span data-stu-id="fbbe8-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="fbbe8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fbbe8-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbbe8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fbbe8-105">DESCRIPTION</span></span>
<span data-ttu-id="fbbe8-106">A **New-AzStackEdgeStorageAccount** parancsmag létrehoz egy új Edge Storage-fiókot egy Stack Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="fbbe8-106">The **New-AzStackEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Stack Edge device.</span></span> <span data-ttu-id="fbbe8-107">Egy eszköz esetén egy Edge Storage-fióknak legalább egy felhőbeli tárfióknak lehet megfeleltetve.</span><span class="sxs-lookup"><span data-stu-id="fbbe8-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="fbbe8-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fbbe8-108">EXAMPLES</span></span>

### <span data-ttu-id="fbbe8-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="fbbe8-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="fbbe8-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="fbbe8-110">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="fbbe8-111">2 EdgeStorageAccounts az eszközön nem oszthat meg több mint 1 felhőalapú tárfiókot</span><span class="sxs-lookup"><span data-stu-id="fbbe8-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="fbbe8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbbe8-112">PARAMETERS</span></span>

### <span data-ttu-id="fbbe8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbbe8-113">-AsJob</span></span>
<span data-ttu-id="fbbe8-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fbbe8-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbe8-115">-Cloud</span><span class="sxs-lookup"><span data-stu-id="fbbe8-115">-Cloud</span></span>
<span data-ttu-id="fbbe8-116">CloudStorageAccount rétegezést fog használni</span><span class="sxs-lookup"><span data-stu-id="fbbe8-116">Will use a CloudStorageAccount for tiering</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbbe8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbbe8-117">-DefaultProfile</span></span>
<span data-ttu-id="fbbe8-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fbbe8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbe8-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="fbbe8-119">-DeviceName</span></span>
<span data-ttu-id="fbbe8-120">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="fbbe8-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbbe8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fbbe8-121">-Name</span></span>
<span data-ttu-id="fbbe8-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="fbbe8-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeStorageAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbe8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbbe8-123">-ResourceGroupName</span></span>
<span data-ttu-id="fbbe8-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="fbbe8-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbbe8-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="fbbe8-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="fbbe8-126">Meglévő StorageAccountCredential erőforrásnévének meg kell adnia</span><span class="sxs-lookup"><span data-stu-id="fbbe8-126">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbbe8-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbbe8-127">-Confirm</span></span>
<span data-ttu-id="fbbe8-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fbbe8-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbe8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbbe8-129">-WhatIf</span></span>
<span data-ttu-id="fbbe8-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fbbe8-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbbe8-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fbbe8-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbe8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbbe8-132">CommonParameters</span></span>
<span data-ttu-id="fbbe8-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbbe8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbbe8-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbbe8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbbe8-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fbbe8-135">INPUTS</span></span>

### <span data-ttu-id="fbbe8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="fbbe8-136">System.String</span></span>

### <span data-ttu-id="fbbe8-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fbbe8-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fbbe8-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbbe8-138">OUTPUTS</span></span>

### <span data-ttu-id="fbbe8-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fbbe8-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="fbbe8-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fbbe8-140">NOTES</span></span>

## <span data-ttu-id="fbbe8-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbbe8-141">RELATED LINKS</span></span>
