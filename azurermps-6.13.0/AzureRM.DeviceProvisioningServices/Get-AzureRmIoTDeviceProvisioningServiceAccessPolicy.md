---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: e0685e82a4db2c786d4bb578544f6cbbd5dbadc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491936"
---
# <span data-ttu-id="5a267-101">Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5a267-101">Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="5a267-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a267-102">SYNOPSIS</span></span>
<span data-ttu-id="5a267-103">Az Azure IoT hub-eszközök kiépítési szolgáltatásában a megosztott hozzáférésű házirendek teljes listája vagy megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="5a267-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a267-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a267-104">SYNTAX</span></span>

### <span data-ttu-id="5a267-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5a267-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a267-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5a267-106">InputObjectSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a267-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5a267-107">ResourceIdSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a267-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a267-108">DESCRIPTION</span></span>
<span data-ttu-id="5a267-109">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="5a267-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="5a267-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5a267-110">EXAMPLES</span></span>

### <span data-ttu-id="5a267-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5a267-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="5a267-112">Az összes megosztott elérési házirend listázása az "myiotdps"-ban</span><span class="sxs-lookup"><span data-stu-id="5a267-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="5a267-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="5a267-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="5a267-114">A "mypolicy" megosztott hozzáférésű házirend részleteinek megjelenítése az Azure IoT hub eszközök kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="5a267-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5a267-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a267-115">PARAMETERS</span></span>

### <span data-ttu-id="5a267-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a267-116">-DefaultProfile</span></span>
<span data-ttu-id="5a267-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a267-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a267-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="5a267-118">-DpsObject</span></span>
<span data-ttu-id="5a267-119">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="5a267-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a267-120">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="5a267-120">-KeyName</span></span>
<span data-ttu-id="5a267-121">A IoT eszköz kiépítési szolgáltatásának elérhetőségi házirendjének neve</span><span class="sxs-lookup"><span data-stu-id="5a267-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="5a267-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5a267-122">-Name</span></span>
<span data-ttu-id="5a267-123">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="5a267-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5a267-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a267-124">-ResourceGroupName</span></span>
<span data-ttu-id="5a267-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5a267-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5a267-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a267-126">-ResourceId</span></span>
<span data-ttu-id="5a267-127">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="5a267-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5a267-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a267-128">CommonParameters</span></span>
<span data-ttu-id="5a267-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a267-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a267-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a267-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a267-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a267-131">INPUTS</span></span>

### <span data-ttu-id="5a267-132">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="5a267-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="5a267-133">Paraméterek: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5a267-133">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="5a267-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5a267-134">System.String</span></span>

## <span data-ttu-id="5a267-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a267-135">OUTPUTS</span></span>

### <span data-ttu-id="5a267-136">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="5a267-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="5a267-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a267-137">NOTES</span></span>

## <span data-ttu-id="5a267-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a267-138">RELATED LINKS</span></span>
