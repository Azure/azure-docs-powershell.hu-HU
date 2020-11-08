---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 87c6bdd72229baec8e65c40d4e2e4309bde59aba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185522"
---
# <span data-ttu-id="770b5-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="770b5-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="770b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="770b5-102">SYNOPSIS</span></span>
<span data-ttu-id="770b5-103">Az Azure IoT hub-eszközök kiépítési szolgáltatásában a megosztott hozzáférésű házirendek teljes listája vagy megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="770b5-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="770b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="770b5-104">SYNTAX</span></span>

### <span data-ttu-id="770b5-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="770b5-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="770b5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="770b5-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="770b5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="770b5-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="770b5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="770b5-108">DESCRIPTION</span></span>
<span data-ttu-id="770b5-109">Az Azure IoT hub eszközök kiépítési szolgáltatásának bevezetéséhez lásd: https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="770b5-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="770b5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="770b5-110">EXAMPLES</span></span>

### <span data-ttu-id="770b5-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="770b5-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="770b5-112">Az összes megosztott elérési házirend listázása az "myiotdps"-ban</span><span class="sxs-lookup"><span data-stu-id="770b5-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="770b5-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="770b5-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="770b5-114">A "mypolicy" megosztott hozzáférésű házirend részleteinek megjelenítése az Azure IoT hub eszközök kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="770b5-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="770b5-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="770b5-115">PARAMETERS</span></span>

### <span data-ttu-id="770b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770b5-116">-DefaultProfile</span></span>
<span data-ttu-id="770b5-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="770b5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="770b5-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="770b5-118">-DpsObject</span></span>
<span data-ttu-id="770b5-119">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="770b5-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="770b5-120">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="770b5-120">-KeyName</span></span>
<span data-ttu-id="770b5-121">A IoT eszköz kiépítési szolgáltatásának elérhetőségi házirendjének neve</span><span class="sxs-lookup"><span data-stu-id="770b5-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="770b5-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="770b5-122">-Name</span></span>
<span data-ttu-id="770b5-123">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="770b5-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="770b5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="770b5-124">-ResourceGroupName</span></span>
<span data-ttu-id="770b5-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="770b5-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="770b5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="770b5-126">-ResourceId</span></span>
<span data-ttu-id="770b5-127">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="770b5-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="770b5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770b5-128">CommonParameters</span></span>
<span data-ttu-id="770b5-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="770b5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770b5-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="770b5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770b5-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="770b5-131">INPUTS</span></span>

### <span data-ttu-id="770b5-132">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="770b5-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="770b5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="770b5-133">System.String</span></span>

## <span data-ttu-id="770b5-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="770b5-134">OUTPUTS</span></span>

### <span data-ttu-id="770b5-135">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="770b5-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="770b5-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="770b5-136">NOTES</span></span>

## <span data-ttu-id="770b5-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="770b5-137">RELATED LINKS</span></span>