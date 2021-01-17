---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
ms.openlocfilehash: ca2381ecff9822bac7a4613566e2da42e79cc5b7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371138"
---
# <span data-ttu-id="025ac-101">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="025ac-101">Get-AzIotHubModule</span></span>

## <span data-ttu-id="025ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="025ac-102">SYNOPSIS</span></span>
<span data-ttu-id="025ac-103">Az IoT-központban található IoT-eszközön található IoT-eszközmodulok vagy -listamodulok részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="025ac-103">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="025ac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="025ac-104">SYNTAX</span></span>

### <span data-ttu-id="025ac-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="025ac-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="025ac-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="025ac-106">InputObjectSet</span></span>
```
Get-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="025ac-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="025ac-107">ResourceIdSet</span></span>
```
Get-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="025ac-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="025ac-108">DESCRIPTION</span></span>
<span data-ttu-id="025ac-109">Az IoT-központban található IoT-eszközön található IoT-eszközmodulok vagy -listamodulok részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="025ac-109">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="025ac-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="025ac-110">EXAMPLES</span></span>

### <span data-ttu-id="025ac-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="025ac-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"

ModuleId                   : myModule1
DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
ManagedBy                  :
```

<span data-ttu-id="025ac-112">Az IoT-központban lekérte egy IoT-eszközmodul részleteit.</span><span class="sxs-lookup"><span data-stu-id="025ac-112">Get the details of an IoT device module in an IoT Hub.</span></span>

### <span data-ttu-id="025ac-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="025ac-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" 

Module Id Device Id Connection State Authentication Last Activity Time
--------- --------- ---------------- -------------- ------------------
module1   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
module2   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
```

<span data-ttu-id="025ac-114">Az IoT-központban egy IoT-eszközön található összes modul megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="025ac-114">Show all modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="025ac-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="025ac-115">PARAMETERS</span></span>

### <span data-ttu-id="025ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="025ac-116">-DefaultProfile</span></span>
<span data-ttu-id="025ac-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="025ac-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="025ac-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="025ac-118">-DeviceId</span></span>
<span data-ttu-id="025ac-119">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="025ac-119">Target Device Id.</span></span>

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

### <span data-ttu-id="025ac-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="025ac-120">-InputObject</span></span>
<span data-ttu-id="025ac-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="025ac-121">IotHub object</span></span>

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

### <span data-ttu-id="025ac-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="025ac-122">-IotHubName</span></span>
<span data-ttu-id="025ac-123">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="025ac-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="025ac-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="025ac-124">-ModuleId</span></span>
<span data-ttu-id="025ac-125">Célmodul-azonosító.</span><span class="sxs-lookup"><span data-stu-id="025ac-125">Target Module Id.</span></span>

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

### <span data-ttu-id="025ac-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="025ac-126">-ResourceGroupName</span></span>
<span data-ttu-id="025ac-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="025ac-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="025ac-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="025ac-128">-ResourceId</span></span>
<span data-ttu-id="025ac-129">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="025ac-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="025ac-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="025ac-130">CommonParameters</span></span>
<span data-ttu-id="025ac-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="025ac-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="025ac-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="025ac-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="025ac-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="025ac-133">INPUTS</span></span>

### <span data-ttu-id="025ac-134">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="025ac-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="025ac-135">System.String</span><span class="sxs-lookup"><span data-stu-id="025ac-135">System.String</span></span>

## <span data-ttu-id="025ac-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="025ac-136">OUTPUTS</span></span>

### <span data-ttu-id="025ac-137">Microsoft.Azure.Commands.Management.iotHub.Models.PSModule</span><span class="sxs-lookup"><span data-stu-id="025ac-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

### <span data-ttu-id="025ac-138">Microsoft.Azure.Commands.Management.iotHub.Models.PSModules[]</span><span class="sxs-lookup"><span data-stu-id="025ac-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="025ac-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="025ac-139">NOTES</span></span>

## <span data-ttu-id="025ac-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="025ac-140">RELATED LINKS</span></span>
