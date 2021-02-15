---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
ms.openlocfilehash: 14e5bbc222bf92f95d77277c6f8d82f578efd0b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152978"
---
# <span data-ttu-id="4a73e-101">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="4a73e-101">Get-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="4a73e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a73e-102">SYNOPSIS</span></span>
<span data-ttu-id="4a73e-103">Szerezze be a megadott eszköz szülőeszközét.</span><span class="sxs-lookup"><span data-stu-id="4a73e-103">Get the parent device of the specified device.</span></span>

## <span data-ttu-id="4a73e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4a73e-104">SYNTAX</span></span>

### <span data-ttu-id="4a73e-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4a73e-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a73e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4a73e-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a73e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4a73e-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a73e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4a73e-108">DESCRIPTION</span></span>
<span data-ttu-id="4a73e-109">Szerezze be a megadott nem edge-eszköz szülőeszközét.</span><span class="sxs-lookup"><span data-stu-id="4a73e-109">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="4a73e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4a73e-110">EXAMPLES</span></span>

### <span data-ttu-id="4a73e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="4a73e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId                   : myParentDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Enabled
StatusReason               : 
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : True
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

<span data-ttu-id="4a73e-112">Szerezze be a megadott nem edge-eszköz szülőeszközét.</span><span class="sxs-lookup"><span data-stu-id="4a73e-112">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="4a73e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a73e-113">PARAMETERS</span></span>

### <span data-ttu-id="4a73e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a73e-114">-DefaultProfile</span></span>
<span data-ttu-id="4a73e-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4a73e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a73e-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="4a73e-116">-DeviceId</span></span>
<span data-ttu-id="4a73e-117">Nem edge-beli eszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4a73e-117">Id of non-edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a73e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a73e-118">-InputObject</span></span>
<span data-ttu-id="4a73e-119">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="4a73e-119">IotHub object</span></span>

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

### <span data-ttu-id="4a73e-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="4a73e-120">-IotHubName</span></span>
<span data-ttu-id="4a73e-121">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="4a73e-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4a73e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a73e-122">-ResourceGroupName</span></span>
<span data-ttu-id="4a73e-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4a73e-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4a73e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a73e-124">-ResourceId</span></span>
<span data-ttu-id="4a73e-125">IotHub erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="4a73e-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4a73e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a73e-126">CommonParameters</span></span>
<span data-ttu-id="4a73e-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a73e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a73e-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a73e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a73e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a73e-129">INPUTS</span></span>

### <span data-ttu-id="4a73e-130">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4a73e-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4a73e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="4a73e-131">System.String</span></span>

## <span data-ttu-id="4a73e-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a73e-132">OUTPUTS</span></span>

### <span data-ttu-id="4a73e-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="4a73e-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="4a73e-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4a73e-134">NOTES</span></span>

## <span data-ttu-id="4a73e-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a73e-135">RELATED LINKS</span></span>
