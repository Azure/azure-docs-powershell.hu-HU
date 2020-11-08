---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 815b8a7feb22e754302c455c7666f8408c348c92
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195282"
---
# <span data-ttu-id="68d8e-101">New-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="68d8e-101">New-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="68d8e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68d8e-102">SYNOPSIS</span></span>
<span data-ttu-id="68d8e-103">Új peremhálózat-tároló fiókot hoz létre az eszközön.</span><span class="sxs-lookup"><span data-stu-id="68d8e-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="68d8e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68d8e-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68d8e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="68d8e-105">DESCRIPTION</span></span>
<span data-ttu-id="68d8e-106">A **New-AzStackEdgeStorageAccount** parancsmag új peremhálózat-tárolási fiókot hoz létre a halom szélén lévő eszközön.</span><span class="sxs-lookup"><span data-stu-id="68d8e-106">The **New-AzStackEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Stack Edge device.</span></span> <span data-ttu-id="68d8e-107">Egy eszköz esetében az egyoldalas tárterületet legfeljebb egyetlen felhőalapú tárterület-fiókhoz lehet rendelni.</span><span class="sxs-lookup"><span data-stu-id="68d8e-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="68d8e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="68d8e-108">EXAMPLES</span></span>

### <span data-ttu-id="68d8e-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="68d8e-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="68d8e-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="68d8e-110">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="68d8e-111">2 EdgeStorageAccounts az eszközön nem lehet több, mint 1 Felhőbeli tárterületet megosztani</span><span class="sxs-lookup"><span data-stu-id="68d8e-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="68d8e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68d8e-112">PARAMETERS</span></span>

### <span data-ttu-id="68d8e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68d8e-113">-AsJob</span></span>
<span data-ttu-id="68d8e-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="68d8e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="68d8e-115">-Felhő</span><span class="sxs-lookup"><span data-stu-id="68d8e-115">-Cloud</span></span>
<span data-ttu-id="68d8e-116">CloudStorageAccount használ a rétegek kiválasztásához</span><span class="sxs-lookup"><span data-stu-id="68d8e-116">Will use a CloudStorageAccount for tiering</span></span>

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

### <span data-ttu-id="68d8e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68d8e-117">-DefaultProfile</span></span>
<span data-ttu-id="68d8e-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68d8e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68d8e-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="68d8e-119">-DeviceName</span></span>
<span data-ttu-id="68d8e-120">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="68d8e-120">Device Name</span></span>

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

### <span data-ttu-id="68d8e-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="68d8e-121">-Name</span></span>
<span data-ttu-id="68d8e-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="68d8e-122">Resource Name</span></span>

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

### <span data-ttu-id="68d8e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68d8e-123">-ResourceGroupName</span></span>
<span data-ttu-id="68d8e-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="68d8e-124">Resource Group Name</span></span>

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

### <span data-ttu-id="68d8e-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="68d8e-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="68d8e-126">A meglévő StorageAccountCredential-erőforrás nevének megadása</span><span class="sxs-lookup"><span data-stu-id="68d8e-126">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="68d8e-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="68d8e-127">-Confirm</span></span>
<span data-ttu-id="68d8e-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="68d8e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68d8e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68d8e-129">-WhatIf</span></span>
<span data-ttu-id="68d8e-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="68d8e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68d8e-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="68d8e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68d8e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68d8e-132">CommonParameters</span></span>
<span data-ttu-id="68d8e-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68d8e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68d8e-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="68d8e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68d8e-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68d8e-135">INPUTS</span></span>

### <span data-ttu-id="68d8e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="68d8e-136">System.String</span></span>

### <span data-ttu-id="68d8e-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="68d8e-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="68d8e-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68d8e-138">OUTPUTS</span></span>

### <span data-ttu-id="68d8e-139">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="68d8e-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="68d8e-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68d8e-140">NOTES</span></span>

## <span data-ttu-id="68d8e-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68d8e-141">RELATED LINKS</span></span>
