---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
ms.openlocfilehash: c1b5c52233b6887dc3221e49174b45d907716c10
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148339"
---
# <span data-ttu-id="c22a3-101">Get-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="c22a3-101">Get-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="c22a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c22a3-102">SYNOPSIS</span></span>
<span data-ttu-id="c22a3-103">Az eszköz rendelési részleteinek lekérte</span><span class="sxs-lookup"><span data-stu-id="c22a3-103">Get the order details for a device</span></span>

## <span data-ttu-id="c22a3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c22a3-104">SYNTAX</span></span>

### <span data-ttu-id="c22a3-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c22a3-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c22a3-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c22a3-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -DeviceObject <PSDataBoxEdgeDevice> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c22a3-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c22a3-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c22a3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c22a3-108">DESCRIPTION</span></span>
<span data-ttu-id="c22a3-109">A **Get-AzDataBoxEdgeOrder** parancsmag megkapja egy Data Box Edge-es eszköz rendelési adatait.</span><span class="sxs-lookup"><span data-stu-id="c22a3-109">The **Get-AzDataBoxEdgeOrder** cmdlet gets the order details for a Data Box Edge device.</span></span> 

## <span data-ttu-id="c22a3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c22a3-110">EXAMPLES</span></span>

### <span data-ttu-id="c22a3-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c22a3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="c22a3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c22a3-112">PARAMETERS</span></span>

### <span data-ttu-id="c22a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c22a3-113">-DefaultProfile</span></span>
<span data-ttu-id="c22a3-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c22a3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c22a3-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c22a3-115">-DeviceName</span></span>
<span data-ttu-id="c22a3-116">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c22a3-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c22a3-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c22a3-117">-DeviceObject</span></span>
<span data-ttu-id="c22a3-118">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="c22a3-118">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c22a3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c22a3-119">-ResourceGroupName</span></span>
<span data-ttu-id="c22a3-120">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c22a3-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c22a3-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c22a3-121">-ResourceId</span></span>
<span data-ttu-id="c22a3-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c22a3-122">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c22a3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c22a3-123">CommonParameters</span></span>
<span data-ttu-id="c22a3-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c22a3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c22a3-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c22a3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c22a3-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c22a3-126">INPUTS</span></span>

### <span data-ttu-id="c22a3-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c22a3-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="c22a3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c22a3-128">System.String</span></span>

## <span data-ttu-id="c22a3-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c22a3-129">OUTPUTS</span></span>

### <span data-ttu-id="c22a3-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="c22a3-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="c22a3-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c22a3-131">NOTES</span></span>

## <span data-ttu-id="c22a3-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c22a3-132">RELATED LINKS</span></span>
