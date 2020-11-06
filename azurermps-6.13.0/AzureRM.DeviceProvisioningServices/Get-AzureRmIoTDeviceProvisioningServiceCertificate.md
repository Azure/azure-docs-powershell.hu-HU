---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: c44e36a0aa08daf7e4a9ae9822f8a4be85db5d57
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491935"
---
# <span data-ttu-id="cdab9-101">Get-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="cdab9-101">Get-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="cdab9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cdab9-102">SYNOPSIS</span></span>
<span data-ttu-id="cdab9-103">Az Azure IoT hub-eszközök kiépítési szolgáltatásában található összes tanúsítvány vagy egy bizonyos tanúsítvány felsorolása.</span><span class="sxs-lookup"><span data-stu-id="cdab9-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdab9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cdab9-104">SYNTAX</span></span>

### <span data-ttu-id="cdab9-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cdab9-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdab9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cdab9-106">InputObjectSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdab9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cdab9-107">ResourceIdSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdab9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cdab9-108">DESCRIPTION</span></span>
<span data-ttu-id="cdab9-109">A CA-tanúsítványok részletes magyarázatát az Azure IoT hub Device kiépítési szolgáltatásban című témakörben találja https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="cdab9-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="cdab9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cdab9-110">EXAMPLES</span></span>

### <span data-ttu-id="cdab9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cdab9-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="cdab9-112">A "mycertificate" részleteinek megjelenítése az Azure IoT hub eszközök kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="cdab9-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="cdab9-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="cdab9-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzureRmIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="cdab9-114">Az összes tanúsítvány listázása a "myiotdps"-ban csővezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="cdab9-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="cdab9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cdab9-115">PARAMETERS</span></span>

### <span data-ttu-id="cdab9-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="cdab9-116">-CertificateName</span></span>
<span data-ttu-id="cdab9-117">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="cdab9-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="cdab9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdab9-118">-DefaultProfile</span></span>
<span data-ttu-id="cdab9-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cdab9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdab9-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="cdab9-120">-DpsObject</span></span>
<span data-ttu-id="cdab9-121">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="cdab9-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="cdab9-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cdab9-122">-Name</span></span>
<span data-ttu-id="cdab9-123">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="cdab9-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="cdab9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdab9-124">-ResourceGroupName</span></span>
<span data-ttu-id="cdab9-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="cdab9-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cdab9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdab9-126">-ResourceId</span></span>
<span data-ttu-id="cdab9-127">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="cdab9-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="cdab9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdab9-128">CommonParameters</span></span>
<span data-ttu-id="cdab9-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cdab9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdab9-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdab9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdab9-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdab9-131">INPUTS</span></span>

### <span data-ttu-id="cdab9-132">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="cdab9-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="cdab9-133">Paraméterek: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cdab9-133">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="cdab9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cdab9-134">System.String</span></span>

## <span data-ttu-id="cdab9-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdab9-135">OUTPUTS</span></span>

### <span data-ttu-id="cdab9-136">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="cdab9-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="cdab9-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cdab9-137">NOTES</span></span>

## <span data-ttu-id="cdab9-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cdab9-138">RELATED LINKS</span></span>
