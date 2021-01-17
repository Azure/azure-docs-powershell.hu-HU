---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
ms.openlocfilehash: 14e5bbc222bf92f95d77277c6f8d82f578efd0b3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364124"
---
# <span data-ttu-id="41c14-101">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="41c14-101">Get-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="41c14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41c14-102">SYNOPSIS</span></span>
<span data-ttu-id="41c14-103">Szerezze be a megadott eszköz szülőeszközét.</span><span class="sxs-lookup"><span data-stu-id="41c14-103">Get the parent device of the specified device.</span></span>

## <span data-ttu-id="41c14-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="41c14-104">SYNTAX</span></span>

### <span data-ttu-id="41c14-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41c14-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41c14-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="41c14-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41c14-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="41c14-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41c14-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="41c14-108">DESCRIPTION</span></span>
<span data-ttu-id="41c14-109">Szerezze be a megadott nem edge-eszköz szülőeszközét.</span><span class="sxs-lookup"><span data-stu-id="41c14-109">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="41c14-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="41c14-110">EXAMPLES</span></span>

### <span data-ttu-id="41c14-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="41c14-111">Example 1</span></span>
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

<span data-ttu-id="41c14-112">Szerezze be a megadott nem edge-eszköz szülőeszközét.</span><span class="sxs-lookup"><span data-stu-id="41c14-112">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="41c14-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41c14-113">PARAMETERS</span></span>

### <span data-ttu-id="41c14-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41c14-114">-DefaultProfile</span></span>
<span data-ttu-id="41c14-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41c14-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41c14-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="41c14-116">-DeviceId</span></span>
<span data-ttu-id="41c14-117">Nem edge-beli eszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="41c14-117">Id of non-edge device.</span></span>

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

### <span data-ttu-id="41c14-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41c14-118">-InputObject</span></span>
<span data-ttu-id="41c14-119">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="41c14-119">IotHub object</span></span>

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

### <span data-ttu-id="41c14-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="41c14-120">-IotHubName</span></span>
<span data-ttu-id="41c14-121">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="41c14-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="41c14-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41c14-122">-ResourceGroupName</span></span>
<span data-ttu-id="41c14-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="41c14-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="41c14-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41c14-124">-ResourceId</span></span>
<span data-ttu-id="41c14-125">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="41c14-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="41c14-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c14-126">CommonParameters</span></span>
<span data-ttu-id="41c14-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41c14-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c14-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41c14-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c14-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41c14-129">INPUTS</span></span>

### <span data-ttu-id="41c14-130">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="41c14-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="41c14-131">System.String</span><span class="sxs-lookup"><span data-stu-id="41c14-131">System.String</span></span>

## <span data-ttu-id="41c14-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41c14-132">OUTPUTS</span></span>

### <span data-ttu-id="41c14-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="41c14-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="41c14-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="41c14-134">NOTES</span></span>

## <span data-ttu-id="41c14-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41c14-135">RELATED LINKS</span></span>
