---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 22f8d81ca68c0136802500876102fa53f8ea7a9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931905"
---
# <span data-ttu-id="8db63-101">New-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8db63-101">New-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="8db63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8db63-102">SYNOPSIS</span></span>
<span data-ttu-id="8db63-103">Létrehoz egy új tárolót az eszköz Edge Storage-fiókjában.</span><span class="sxs-lookup"><span data-stu-id="8db63-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="8db63-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8db63-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8db63-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8db63-105">DESCRIPTION</span></span>
<span data-ttu-id="8db63-106">A **New-AzDataBoxEdgeStorageContainer** parancsmag új tárolót hoz létre a Edge Storage-fiókban egy Data Box Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="8db63-106">The **New-AzDataBoxEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Data Box Edge device.</span></span>

## <span data-ttu-id="8db63-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8db63-107">EXAMPLES</span></span>

### <span data-ttu-id="8db63-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="8db63-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="8db63-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8db63-109">PARAMETERS</span></span>

### <span data-ttu-id="8db63-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8db63-110">-AsJob</span></span>
<span data-ttu-id="8db63-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8db63-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8db63-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="8db63-112">-DataFormat</span></span>
<span data-ttu-id="8db63-113">Adatformátum beállítása például: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="8db63-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db63-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8db63-114">-DefaultProfile</span></span>
<span data-ttu-id="8db63-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8db63-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8db63-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8db63-116">-DeviceName</span></span>
<span data-ttu-id="8db63-117">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="8db63-117">Device Name</span></span>

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

### <span data-ttu-id="8db63-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8db63-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="8db63-119">Meglévő EdgeStorageAccount nevének meg kell adnia</span><span class="sxs-lookup"><span data-stu-id="8db63-119">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db63-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8db63-120">-Name</span></span>
<span data-ttu-id="8db63-121">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="8db63-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db63-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8db63-122">-ResourceGroupName</span></span>
<span data-ttu-id="8db63-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8db63-123">Resource Group Name</span></span>

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

### <span data-ttu-id="8db63-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8db63-124">-Confirm</span></span>
<span data-ttu-id="8db63-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8db63-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8db63-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8db63-126">-WhatIf</span></span>
<span data-ttu-id="8db63-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8db63-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8db63-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8db63-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8db63-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8db63-129">CommonParameters</span></span>
<span data-ttu-id="8db63-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8db63-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8db63-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8db63-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8db63-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8db63-132">INPUTS</span></span>

### <span data-ttu-id="8db63-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8db63-133">System.String</span></span>

## <span data-ttu-id="8db63-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8db63-134">OUTPUTS</span></span>

### <span data-ttu-id="8db63-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8db63-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="8db63-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8db63-136">NOTES</span></span>

## <span data-ttu-id="8db63-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8db63-137">RELATED LINKS</span></span>
