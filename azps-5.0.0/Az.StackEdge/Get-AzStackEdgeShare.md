---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
ms.openlocfilehash: 0e0d0e3b2dfca824d66a9a75f3e22438335c97db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186944"
---
# <span data-ttu-id="f2812-101">Get-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="f2812-101">Get-AzStackEdgeShare</span></span>

## <span data-ttu-id="f2812-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2812-102">SYNOPSIS</span></span>
<span data-ttu-id="f2812-103">Az eszköz számára elérhető megosztásokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f2812-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="f2812-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2812-104">SYNTAX</span></span>

### <span data-ttu-id="f2812-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f2812-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2812-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2812-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2812-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2812-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2812-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2812-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="f2812-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2812-109">DESCRIPTION</span></span>
<span data-ttu-id="f2812-110">A **Get-AzStackEdgeShare** parancsmag az elérhető megosztásokat kapja egy halom Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="f2812-110">The **Get-AzStackEdgeShare** cmdlet gets the available shares for a Stack Edge device.</span></span> <span data-ttu-id="f2812-111">Ha a név meg van jelenítve, akkor a megosztást a név alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f2812-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="f2812-112">Példák</span><span class="sxs-lookup"><span data-stu-id="f2812-112">EXAMPLES</span></span>

### <span data-ttu-id="f2812-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f2812-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="f2812-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2812-114">PARAMETERS</span></span>

### <span data-ttu-id="f2812-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2812-115">-DefaultProfile</span></span>
<span data-ttu-id="f2812-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2812-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2812-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f2812-117">-DeviceName</span></span>
<span data-ttu-id="f2812-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="f2812-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2812-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="f2812-119">-DeviceObject</span></span>
<span data-ttu-id="f2812-120">Adja meg a megfelelő eszköz-objektumot</span><span class="sxs-lookup"><span data-stu-id="f2812-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2812-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f2812-121">-Name</span></span>
<span data-ttu-id="f2812-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="f2812-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeShareName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2812-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2812-123">-ResourceGroupName</span></span>
<span data-ttu-id="f2812-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f2812-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2812-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2812-125">-ResourceId</span></span>
<span data-ttu-id="f2812-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2812-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="f2812-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2812-127">CommonParameters</span></span>
<span data-ttu-id="f2812-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2812-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2812-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f2812-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2812-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2812-130">INPUTS</span></span>

### <span data-ttu-id="f2812-131">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f2812-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="f2812-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2812-132">OUTPUTS</span></span>

### <span data-ttu-id="f2812-133">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="f2812-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="f2812-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2812-134">NOTES</span></span>

## <span data-ttu-id="f2812-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2812-135">RELATED LINKS</span></span>
