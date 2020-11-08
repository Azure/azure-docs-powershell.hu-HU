---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 30926eaad6447f109b1755d419be0b3931a76054
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184920"
---
# <span data-ttu-id="808e4-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="808e4-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="808e4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="808e4-102">SYNOPSIS</span></span>
<span data-ttu-id="808e4-103">Megtudhatja, hogy milyen kapcsolati karakterláncot hoz létre a TARGET IoT Device Module egy IOT-központban.</span><span class="sxs-lookup"><span data-stu-id="808e4-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="808e4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="808e4-104">SYNTAX</span></span>

### <span data-ttu-id="808e4-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="808e4-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="808e4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="808e4-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="808e4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="808e4-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="808e4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="808e4-108">DESCRIPTION</span></span>
<span data-ttu-id="808e4-109">Az Azure IoT központi verziójában található IoT-eszközök minden moduljának vagy meghatározott moduljának listája kapcsolati karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="808e4-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="808e4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="808e4-110">EXAMPLES</span></span>

### <span data-ttu-id="808e4-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="808e4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="808e4-112">A IoT-eszközök minden modul kapcsolati karakterláncának megjelenítése egy IOT-központban.</span><span class="sxs-lookup"><span data-stu-id="808e4-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="808e4-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="808e4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="808e4-114">A másodlagos modul kapcsolati karakterláncát beolvashatja egy IOT-hub IoT-eszközéhez.</span><span class="sxs-lookup"><span data-stu-id="808e4-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="808e4-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="808e4-115">PARAMETERS</span></span>

### <span data-ttu-id="808e4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="808e4-116">-DefaultProfile</span></span>
<span data-ttu-id="808e4-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="808e4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="808e4-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="808e4-118">-DeviceId</span></span>
<span data-ttu-id="808e4-119">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="808e4-119">Target Device Id.</span></span>

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

### <span data-ttu-id="808e4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="808e4-120">-InputObject</span></span>
<span data-ttu-id="808e4-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="808e4-121">IotHub object</span></span>

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

### <span data-ttu-id="808e4-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="808e4-122">-IotHubName</span></span>
<span data-ttu-id="808e4-123">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="808e4-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="808e4-124">-Típus</span><span class="sxs-lookup"><span data-stu-id="808e4-124">-KeyType</span></span>
<span data-ttu-id="808e4-125">Megosztott hozzáférés házirend-kulcs típusa az Auth szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="808e4-125">Shared access policy key type for auth.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="808e4-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="808e4-126">-ModuleId</span></span>
<span data-ttu-id="808e4-127">A cél modul azonosítója</span><span class="sxs-lookup"><span data-stu-id="808e4-127">Target Module Id.</span></span>

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

### <span data-ttu-id="808e4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="808e4-128">-ResourceGroupName</span></span>
<span data-ttu-id="808e4-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="808e4-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="808e4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="808e4-130">-ResourceId</span></span>
<span data-ttu-id="808e4-131">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="808e4-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="808e4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="808e4-132">CommonParameters</span></span>
<span data-ttu-id="808e4-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="808e4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="808e4-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="808e4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="808e4-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="808e4-135">INPUTS</span></span>

### <span data-ttu-id="808e4-136">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="808e4-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="808e4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="808e4-137">System.String</span></span>

## <span data-ttu-id="808e4-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="808e4-138">OUTPUTS</span></span>

### <span data-ttu-id="808e4-139">Microsoft. Azure. Command. Management. IotHub. models. PSModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="808e4-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="808e4-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="808e4-140">NOTES</span></span>

## <span data-ttu-id="808e4-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="808e4-141">RELATED LINKS</span></span>