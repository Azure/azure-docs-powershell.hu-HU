---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
ms.openlocfilehash: 6a20f81644827c84ee1ce215ad2e87268650caf9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477266"
---
# <span data-ttu-id="27990-101">Get-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="27990-101">Get-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="27990-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27990-102">SYNOPSIS</span></span>
<span data-ttu-id="27990-103">Az eszközhöz elérhető megosztások lekérhetők.</span><span class="sxs-lookup"><span data-stu-id="27990-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="27990-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="27990-104">SYNTAX</span></span>

### <span data-ttu-id="27990-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27990-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27990-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27990-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27990-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="27990-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27990-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27990-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="27990-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="27990-109">DESCRIPTION</span></span>
<span data-ttu-id="27990-110">A **Get-AzDataBoxEdgeShare** parancsmag megkapja a rendelkezésre álló megosztásokat egy Data Box Edge-eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="27990-110">The **Get-AzDataBoxEdgeShare** cmdlet gets the available shares for a Data Box Edge device.</span></span> <span data-ttu-id="27990-111">Ha a Név meg van biztosítanak, akkor a megosztás név szerint történik.</span><span class="sxs-lookup"><span data-stu-id="27990-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="27990-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="27990-112">EXAMPLES</span></span>

### <span data-ttu-id="27990-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="27990-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="27990-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27990-114">PARAMETERS</span></span>

### <span data-ttu-id="27990-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27990-115">-DefaultProfile</span></span>
<span data-ttu-id="27990-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27990-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27990-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="27990-117">-DeviceName</span></span>
<span data-ttu-id="27990-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="27990-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27990-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="27990-119">-DeviceObject</span></span>
<span data-ttu-id="27990-120">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="27990-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27990-121">-Name</span><span class="sxs-lookup"><span data-stu-id="27990-121">-Name</span></span>
<span data-ttu-id="27990-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="27990-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27990-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27990-123">-ResourceGroupName</span></span>
<span data-ttu-id="27990-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="27990-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27990-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27990-125">-ResourceId</span></span>
<span data-ttu-id="27990-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="27990-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27990-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27990-127">CommonParameters</span></span>
<span data-ttu-id="27990-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27990-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27990-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27990-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27990-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27990-130">INPUTS</span></span>

### <span data-ttu-id="27990-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="27990-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="27990-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27990-132">OUTPUTS</span></span>

### <span data-ttu-id="27990-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="27990-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="27990-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="27990-134">NOTES</span></span>

## <span data-ttu-id="27990-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27990-135">RELATED LINKS</span></span>
