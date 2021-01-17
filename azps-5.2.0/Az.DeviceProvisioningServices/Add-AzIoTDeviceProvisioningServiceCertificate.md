---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: d4dcf52a3a705042f994c8106bd931a8b704a049
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340973"
---
# <span data-ttu-id="7786b-101">Add-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="7786b-101">Add-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="7786b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7786b-102">SYNOPSIS</span></span>
<span data-ttu-id="7786b-103">Azure IoT Hub eszköz kiépítési szolgáltatás tanúsítványának létrehozása/frissítése.</span><span class="sxs-lookup"><span data-stu-id="7786b-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="7786b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7786b-104">SYNTAX</span></span>

### <span data-ttu-id="7786b-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7786b-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7786b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7786b-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7786b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7786b-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7786b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7786b-108">DESCRIPTION</span></span>
<span data-ttu-id="7786b-109">Feltölt egy új tanúsítványt, vagy lecseréli a meglévő tanúsítványt ugyanazra a névre.</span><span class="sxs-lookup"><span data-stu-id="7786b-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="7786b-110">Az Azure IoT Hub eszköz kiépítési szolgáltatásában található hitelesítésszolgáltatói tanúsítványok részletes magyarázatát https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates lásd: .</span><span class="sxs-lookup"><span data-stu-id="7786b-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="7786b-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7786b-111">EXAMPLES</span></span>

### <span data-ttu-id="7786b-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="7786b-112">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

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

<span data-ttu-id="7786b-113">Töltsön fel egy tanúsítványszolgáltatói tanúsítványfájlt egy Azure IoT-központbeli eszköz kiépítési szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="7786b-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="7786b-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="7786b-114">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="7786b-115">Egy új CER-fájl feltöltésével frissíti a hitelesítésszolgáltatói tanúsítványt egy központi IoT-eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="7786b-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="7786b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7786b-116">PARAMETERS</span></span>

### <span data-ttu-id="7786b-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="7786b-117">-CertificateName</span></span>
<span data-ttu-id="7786b-118">Az Iot-eszköz kiépítési szolgáltatás tanúsítványának neve</span><span class="sxs-lookup"><span data-stu-id="7786b-118">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="7786b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7786b-119">-DefaultProfile</span></span>
<span data-ttu-id="7786b-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7786b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7786b-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="7786b-121">-Etag</span></span>
<span data-ttu-id="7786b-122">A tanúsítvány etagja</span><span class="sxs-lookup"><span data-stu-id="7786b-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="7786b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7786b-123">-InputObject</span></span>
<span data-ttu-id="7786b-124">IoT-eszköz kiépítési szolgáltatás tanúsítványobjektuma</span><span class="sxs-lookup"><span data-stu-id="7786b-124">IoT Device Provisioning Service Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7786b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7786b-125">-Name</span></span>
<span data-ttu-id="7786b-126">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="7786b-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7786b-127">-Path</span><span class="sxs-lookup"><span data-stu-id="7786b-127">-Path</span></span>
<span data-ttu-id="7786b-128">Base-64 representation of X509 certificate .cer file or .pem file path</span><span class="sxs-lookup"><span data-stu-id="7786b-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7786b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7786b-129">-ResourceGroupName</span></span>
<span data-ttu-id="7786b-130">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7786b-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7786b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7786b-131">-ResourceId</span></span>
<span data-ttu-id="7786b-132">IoT-eszköz kiépítési szolgáltatás tanúsítványának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="7786b-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="7786b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7786b-133">-Confirm</span></span>
<span data-ttu-id="7786b-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7786b-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7786b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7786b-135">-WhatIf</span></span>
<span data-ttu-id="7786b-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7786b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7786b-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7786b-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7786b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7786b-138">CommonParameters</span></span>
<span data-ttu-id="7786b-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7786b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7786b-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7786b-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7786b-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7786b-141">INPUTS</span></span>

### <span data-ttu-id="7786b-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="7786b-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="7786b-143">System.String</span><span class="sxs-lookup"><span data-stu-id="7786b-143">System.String</span></span>

## <span data-ttu-id="7786b-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7786b-144">OUTPUTS</span></span>

### <span data-ttu-id="7786b-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="7786b-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="7786b-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7786b-146">NOTES</span></span>

## <span data-ttu-id="7786b-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7786b-147">RELATED LINKS</span></span>
