---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
ms.openlocfilehash: 616830906621b673010ca8708b909608c06f93fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942946"
---
# <span data-ttu-id="a35ef-101">Get-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="a35ef-101">Get-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="a35ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a35ef-102">SYNOPSIS</span></span>
<span data-ttu-id="a35ef-103">Az eszközhöz elérhető megosztások lekérhetők.</span><span class="sxs-lookup"><span data-stu-id="a35ef-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="a35ef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a35ef-104">SYNTAX</span></span>

### <span data-ttu-id="a35ef-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a35ef-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a35ef-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a35ef-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a35ef-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a35ef-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a35ef-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a35ef-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="a35ef-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a35ef-109">DESCRIPTION</span></span>
<span data-ttu-id="a35ef-110">A **Get-AzDataBoxEdgeShare** parancsmag megkapja a rendelkezésre álló megosztásokat egy Data Box Edge-eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="a35ef-110">The **Get-AzDataBoxEdgeShare** cmdlet gets the available shares for a Data Box Edge device.</span></span> <span data-ttu-id="a35ef-111">Ha a Név meg van biztosítanak, akkor a megosztás név szerint történik.</span><span class="sxs-lookup"><span data-stu-id="a35ef-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="a35ef-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a35ef-112">EXAMPLES</span></span>

### <span data-ttu-id="a35ef-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="a35ef-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="a35ef-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a35ef-114">PARAMETERS</span></span>

### <span data-ttu-id="a35ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a35ef-115">-DefaultProfile</span></span>
<span data-ttu-id="a35ef-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a35ef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a35ef-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a35ef-117">-DeviceName</span></span>
<span data-ttu-id="a35ef-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="a35ef-118">Device Name</span></span>

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

### <span data-ttu-id="a35ef-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="a35ef-119">-DeviceObject</span></span>
<span data-ttu-id="a35ef-120">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="a35ef-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="a35ef-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a35ef-121">-Name</span></span>
<span data-ttu-id="a35ef-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="a35ef-122">Resource Name</span></span>

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

### <span data-ttu-id="a35ef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a35ef-123">-ResourceGroupName</span></span>
<span data-ttu-id="a35ef-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a35ef-124">Resource Group Name</span></span>

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

### <span data-ttu-id="a35ef-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a35ef-125">-ResourceId</span></span>
<span data-ttu-id="a35ef-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a35ef-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="a35ef-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a35ef-127">CommonParameters</span></span>
<span data-ttu-id="a35ef-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a35ef-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a35ef-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a35ef-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a35ef-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a35ef-130">INPUTS</span></span>

### <span data-ttu-id="a35ef-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a35ef-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="a35ef-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a35ef-132">OUTPUTS</span></span>

### <span data-ttu-id="a35ef-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="a35ef-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="a35ef-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a35ef-134">NOTES</span></span>

## <span data-ttu-id="a35ef-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a35ef-135">RELATED LINKS</span></span>
