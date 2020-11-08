---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
ms.openlocfilehash: 2ef7b7ac2a06da0ef0f4b09d82f9a4ed447618ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182094"
---
# <span data-ttu-id="aa765-101">Get-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="aa765-101">Get-AzStackEdgeOrder</span></span>

## <span data-ttu-id="aa765-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa765-102">SYNOPSIS</span></span>
<span data-ttu-id="aa765-103">Az eszközök rendeléséhez szükséges adatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="aa765-103">Get the order details for a device</span></span>

## <span data-ttu-id="aa765-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa765-104">SYNTAX</span></span>

### <span data-ttu-id="aa765-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aa765-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa765-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa765-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzStackEdgeOrder -DeviceObject <PSStackEdgeOrder> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aa765-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa765-107">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa765-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa765-108">DESCRIPTION</span></span>
<span data-ttu-id="aa765-109">A **Get-AzStackEdgeOrder** parancsmag a halom szélén álló eszközök rendelésének részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aa765-109">The **Get-AzStackEdgeOrder** cmdlet gets the order details for a Stack Edge device.</span></span> 

## <span data-ttu-id="aa765-110">Példák</span><span class="sxs-lookup"><span data-stu-id="aa765-110">EXAMPLES</span></span>

### <span data-ttu-id="aa765-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aa765-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="aa765-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa765-112">PARAMETERS</span></span>

### <span data-ttu-id="aa765-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa765-113">-DefaultProfile</span></span>
<span data-ttu-id="aa765-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa765-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa765-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="aa765-115">-DeviceName</span></span>
<span data-ttu-id="aa765-116">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="aa765-116">Resource Group Name</span></span>

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

### <span data-ttu-id="aa765-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="aa765-117">-DeviceObject</span></span>
<span data-ttu-id="aa765-118">Adja meg a megfelelő eszköz-objektumot</span><span class="sxs-lookup"><span data-stu-id="aa765-118">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: GetByDeviceObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa765-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa765-119">-ResourceGroupName</span></span>
<span data-ttu-id="aa765-120">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="aa765-120">Resource Group Name</span></span>

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

### <span data-ttu-id="aa765-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa765-121">-ResourceId</span></span>
<span data-ttu-id="aa765-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa765-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="aa765-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa765-123">CommonParameters</span></span>
<span data-ttu-id="aa765-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa765-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa765-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="aa765-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa765-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa765-126">INPUTS</span></span>

### <span data-ttu-id="aa765-127">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="aa765-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

### <span data-ttu-id="aa765-128">System. String</span><span class="sxs-lookup"><span data-stu-id="aa765-128">System.String</span></span>

## <span data-ttu-id="aa765-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa765-129">OUTPUTS</span></span>

### <span data-ttu-id="aa765-130">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="aa765-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="aa765-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa765-131">NOTES</span></span>

## <span data-ttu-id="aa765-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa765-132">RELATED LINKS</span></span>
