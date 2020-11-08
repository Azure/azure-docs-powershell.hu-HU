---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
ms.openlocfilehash: c1b5c52233b6887dc3221e49174b45d907716c10
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025429"
---
# <span data-ttu-id="e7a77-101">Get-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="e7a77-101">Get-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="e7a77-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7a77-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a77-103">Az eszközök rendeléséhez szükséges adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="e7a77-103">Get the order details for a device</span></span>

## <span data-ttu-id="e7a77-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7a77-104">SYNTAX</span></span>

### <span data-ttu-id="e7a77-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e7a77-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7a77-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7a77-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -DeviceObject <PSDataBoxEdgeDevice> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7a77-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7a77-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7a77-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7a77-108">DESCRIPTION</span></span>
<span data-ttu-id="e7a77-109">A **Get-AzDataBoxEdgeOrder** parancsmag az adatmező Edge-eszközéhez rendeli a rendelés részleteit.</span><span class="sxs-lookup"><span data-stu-id="e7a77-109">The **Get-AzDataBoxEdgeOrder** cmdlet gets the order details for a Data Box Edge device.</span></span> 

## <span data-ttu-id="e7a77-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e7a77-110">EXAMPLES</span></span>

### <span data-ttu-id="e7a77-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e7a77-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="e7a77-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7a77-112">PARAMETERS</span></span>

### <span data-ttu-id="e7a77-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a77-113">-DefaultProfile</span></span>
<span data-ttu-id="e7a77-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7a77-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7a77-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e7a77-115">-DeviceName</span></span>
<span data-ttu-id="e7a77-116">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e7a77-116">Resource Group Name</span></span>

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

### <span data-ttu-id="e7a77-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="e7a77-117">-DeviceObject</span></span>
<span data-ttu-id="e7a77-118">Adja meg a megfelelő eszköz-objektumot</span><span class="sxs-lookup"><span data-stu-id="e7a77-118">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="e7a77-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7a77-119">-ResourceGroupName</span></span>
<span data-ttu-id="e7a77-120">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e7a77-120">Resource Group Name</span></span>

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

### <span data-ttu-id="e7a77-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7a77-121">-ResourceId</span></span>
<span data-ttu-id="e7a77-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7a77-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="e7a77-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a77-123">CommonParameters</span></span>
<span data-ttu-id="e7a77-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7a77-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a77-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e7a77-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a77-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7a77-126">INPUTS</span></span>

### <span data-ttu-id="e7a77-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e7a77-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="e7a77-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e7a77-128">System.String</span></span>

## <span data-ttu-id="e7a77-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7a77-129">OUTPUTS</span></span>

### <span data-ttu-id="e7a77-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="e7a77-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="e7a77-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7a77-131">NOTES</span></span>

## <span data-ttu-id="e7a77-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7a77-132">RELATED LINKS</span></span>
