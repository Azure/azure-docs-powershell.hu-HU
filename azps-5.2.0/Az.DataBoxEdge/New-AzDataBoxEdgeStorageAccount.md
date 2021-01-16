---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 2a5a1314f422a7b91a5cc8885abe0af98fa395a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334169"
---
# <span data-ttu-id="c8bda-101">New-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8bda-101">New-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="c8bda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8bda-102">SYNOPSIS</span></span>
<span data-ttu-id="c8bda-103">Létrehoz egy új Edge Storage-fiókot az eszközön.</span><span class="sxs-lookup"><span data-stu-id="c8bda-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="c8bda-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c8bda-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8bda-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c8bda-105">DESCRIPTION</span></span>
<span data-ttu-id="c8bda-106">A **New-AzDataBoxEdgeStorageAccount** parancsmag létrehoz egy új Edge Storage-fiókot egy Data Box Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="c8bda-106">The **New-AzDataBoxEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Data Box Edge device.</span></span> <span data-ttu-id="c8bda-107">Egy eszköz esetén egy Edge Storage-fióknak legalább egy felhőbeli tárfióknak lehet megfeleltetve.</span><span class="sxs-lookup"><span data-stu-id="c8bda-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="c8bda-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c8bda-108">EXAMPLES</span></span>

### <span data-ttu-id="c8bda-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="c8bda-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="c8bda-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="c8bda-110">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="c8bda-111">2 EdgeStorageAccounts az eszközön nem oszthat meg több mint 1 felhőalapú tárfiókot</span><span class="sxs-lookup"><span data-stu-id="c8bda-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="c8bda-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8bda-112">PARAMETERS</span></span>

### <span data-ttu-id="c8bda-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8bda-113">-AsJob</span></span>
<span data-ttu-id="c8bda-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c8bda-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8bda-115">-Cloud</span><span class="sxs-lookup"><span data-stu-id="c8bda-115">-Cloud</span></span>
<span data-ttu-id="c8bda-116">CloudStorageAccount rétegezést fog használni</span><span class="sxs-lookup"><span data-stu-id="c8bda-116">Will use a CloudStorageAccount for tiering</span></span>

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

### <span data-ttu-id="c8bda-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8bda-117">-DefaultProfile</span></span>
<span data-ttu-id="c8bda-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8bda-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8bda-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c8bda-119">-DeviceName</span></span>
<span data-ttu-id="c8bda-120">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="c8bda-120">Device Name</span></span>

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

### <span data-ttu-id="c8bda-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c8bda-121">-Name</span></span>
<span data-ttu-id="c8bda-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="c8bda-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8bda-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8bda-123">-ResourceGroupName</span></span>
<span data-ttu-id="c8bda-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c8bda-124">Resource Group Name</span></span>

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

### <span data-ttu-id="c8bda-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="c8bda-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="c8bda-126">Meglévő StorageAccountCredential erőforrásnévének meg kell adnia</span><span class="sxs-lookup"><span data-stu-id="c8bda-126">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="c8bda-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8bda-127">-Confirm</span></span>
<span data-ttu-id="c8bda-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c8bda-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8bda-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8bda-129">-WhatIf</span></span>
<span data-ttu-id="c8bda-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c8bda-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8bda-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c8bda-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8bda-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8bda-132">CommonParameters</span></span>
<span data-ttu-id="c8bda-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8bda-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8bda-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8bda-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8bda-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8bda-135">INPUTS</span></span>

### <span data-ttu-id="c8bda-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c8bda-136">System.String</span></span>

### <span data-ttu-id="c8bda-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c8bda-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c8bda-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8bda-138">OUTPUTS</span></span>

### <span data-ttu-id="c8bda-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8bda-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="c8bda-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c8bda-140">NOTES</span></span>

## <span data-ttu-id="c8bda-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8bda-141">RELATED LINKS</span></span>
