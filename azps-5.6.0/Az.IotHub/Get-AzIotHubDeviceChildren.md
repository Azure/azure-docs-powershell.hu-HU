---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: ec84ee72caadc4d49c29a72e1e5171e589dc11d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936921"
---
# <span data-ttu-id="6a153-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="6a153-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="6a153-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a153-102">SYNOPSIS</span></span>
<span data-ttu-id="6a153-103">A hozzárendelt gyermekeszközök vesszővel elválasztott listájának nyomtatása.</span><span class="sxs-lookup"><span data-stu-id="6a153-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="6a153-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6a153-104">SYNTAX</span></span>

### <span data-ttu-id="6a153-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6a153-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a153-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6a153-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a153-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6a153-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a153-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6a153-108">DESCRIPTION</span></span>
<span data-ttu-id="6a153-109">Az összes hozzárendelt, nem edge-hez rendelt eszköz megjelenítése vesszővel elválasztott listaként az összes peremhálózati eszközről vagy adott eszközről.</span><span class="sxs-lookup"><span data-stu-id="6a153-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="6a153-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6a153-110">EXAMPLES</span></span>

### <span data-ttu-id="6a153-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="6a153-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="6a153-112">Az összes hozzárendelt, nem edge-hez rendelt eszköz megjelenítése vesszővel elválasztott listaként.</span><span class="sxs-lookup"><span data-stu-id="6a153-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="6a153-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="6a153-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="6a153-114">Az összes hozzárendelt, nem edge-hez rendelt eszköz megjelenítése az összes peremhálózati eszköz vesszővel elválasztott listájaként.</span><span class="sxs-lookup"><span data-stu-id="6a153-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="6a153-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a153-115">PARAMETERS</span></span>

### <span data-ttu-id="6a153-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a153-116">-DefaultProfile</span></span>
<span data-ttu-id="6a153-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a153-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a153-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="6a153-118">-DeviceId</span></span>
<span data-ttu-id="6a153-119">A peremhálózati eszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6a153-119">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a153-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a153-120">-InputObject</span></span>
<span data-ttu-id="6a153-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="6a153-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a153-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6a153-122">-IotHubName</span></span>
<span data-ttu-id="6a153-123">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="6a153-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a153-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a153-124">-ResourceGroupName</span></span>
<span data-ttu-id="6a153-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="6a153-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a153-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a153-126">-ResourceId</span></span>
<span data-ttu-id="6a153-127">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="6a153-127">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a153-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a153-128">CommonParameters</span></span>
<span data-ttu-id="6a153-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a153-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a153-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a153-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a153-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a153-131">INPUTS</span></span>

### <span data-ttu-id="6a153-132">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6a153-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6a153-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6a153-133">System.String</span></span>

## <span data-ttu-id="6a153-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a153-134">OUTPUTS</span></span>

### <span data-ttu-id="6a153-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice Minden</span><span class="sxs-lookup"><span data-stu-id="6a153-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="6a153-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesKv[]</span><span class="sxs-lookup"><span data-stu-id="6a153-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="6a153-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6a153-137">NOTES</span></span>

## <span data-ttu-id="6a153-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a153-138">RELATED LINKS</span></span>
