---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
ms.openlocfilehash: 2ef7b7ac2a06da0ef0f4b09d82f9a4ed447618ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346446"
---
# <span data-ttu-id="12048-101">Get-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="12048-101">Get-AzStackEdgeOrder</span></span>

## <span data-ttu-id="12048-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12048-102">SYNOPSIS</span></span>
<span data-ttu-id="12048-103">Eszköz rendelési részleteinek lekérte</span><span class="sxs-lookup"><span data-stu-id="12048-103">Get the order details for a device</span></span>

## <span data-ttu-id="12048-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="12048-104">SYNTAX</span></span>

### <span data-ttu-id="12048-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="12048-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12048-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12048-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzStackEdgeOrder -DeviceObject <PSStackEdgeOrder> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12048-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12048-107">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12048-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="12048-108">DESCRIPTION</span></span>
<span data-ttu-id="12048-109">A **Get-AzStackEdgeOrder** parancsmag a Stack Edge-es eszközök rendelési adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="12048-109">The **Get-AzStackEdgeOrder** cmdlet gets the order details for a Stack Edge device.</span></span> 

## <span data-ttu-id="12048-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="12048-110">EXAMPLES</span></span>

### <span data-ttu-id="12048-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="12048-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="12048-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12048-112">PARAMETERS</span></span>

### <span data-ttu-id="12048-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12048-113">-DefaultProfile</span></span>
<span data-ttu-id="12048-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12048-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12048-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="12048-115">-DeviceName</span></span>
<span data-ttu-id="12048-116">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="12048-116">Resource Group Name</span></span>

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

### <span data-ttu-id="12048-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="12048-117">-DeviceObject</span></span>
<span data-ttu-id="12048-118">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="12048-118">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="12048-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12048-119">-ResourceGroupName</span></span>
<span data-ttu-id="12048-120">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="12048-120">Resource Group Name</span></span>

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

### <span data-ttu-id="12048-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12048-121">-ResourceId</span></span>
<span data-ttu-id="12048-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="12048-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="12048-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12048-123">CommonParameters</span></span>
<span data-ttu-id="12048-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12048-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12048-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12048-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12048-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12048-126">INPUTS</span></span>

### <span data-ttu-id="12048-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="12048-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

### <span data-ttu-id="12048-128">System.String</span><span class="sxs-lookup"><span data-stu-id="12048-128">System.String</span></span>

## <span data-ttu-id="12048-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12048-129">OUTPUTS</span></span>

### <span data-ttu-id="12048-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="12048-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="12048-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="12048-131">NOTES</span></span>

## <span data-ttu-id="12048-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12048-132">RELATED LINKS</span></span>
