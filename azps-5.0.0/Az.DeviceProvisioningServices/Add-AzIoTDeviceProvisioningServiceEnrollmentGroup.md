---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 7c5c2f747b5de24e1ccf3a4cf047930746c0d863
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185529"
---
# <span data-ttu-id="239df-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="239df-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="239df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="239df-102">SYNOPSIS</span></span>
<span data-ttu-id="239df-103">Eszköz-beiktatási csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="239df-103">Create a device enrollment group.</span></span>

## <span data-ttu-id="239df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="239df-104">SYNTAX</span></span>

### <span data-ttu-id="239df-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="239df-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="239df-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="239df-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="239df-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="239df-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="239df-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="239df-108">DESCRIPTION</span></span>
<span data-ttu-id="239df-109">Hozzon létre egy tanúsítványigénylési csoportot egy Azure IoT hub-eszköz kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="239df-109">Create an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="239df-110">Példák</span><span class="sxs-lookup"><span data-stu-id="239df-110">EXAMPLES</span></span>

### <span data-ttu-id="239df-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="239df-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="239df-112">Tanúsítványigénylési típus SymmetricKey létrehozása</span><span class="sxs-lookup"><span data-stu-id="239df-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="239df-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="239df-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="239df-114">Tanúsítványigénylési típus X509 létrehozása</span><span class="sxs-lookup"><span data-stu-id="239df-114">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="239df-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="239df-115">Example 3</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey -tag $tag
```

<span data-ttu-id="239df-116">Hozzon létre egy beiratkozási típust a SymmetricKey és a Initial Twin állammal.</span><span class="sxs-lookup"><span data-stu-id="239df-116">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="239df-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="239df-117">PARAMETERS</span></span>

### <span data-ttu-id="239df-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="239df-118">-AllocationPolicy</span></span>
<span data-ttu-id="239df-119">A hub-hoz rendelt eszközhöz tartozó kiosztás típusa.</span><span class="sxs-lookup"><span data-stu-id="239df-119">Type of allocation for device assigned to the Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAllocationPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="239df-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="239df-120">-ApiVersion</span></span>
<span data-ttu-id="239df-121">A kiépítési szolgáltatás API-változata az egyéni hozzárendelés-kérésben.</span><span class="sxs-lookup"><span data-stu-id="239df-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="239df-122">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="239df-122">-AttestationType</span></span>
<span data-ttu-id="239df-123">Igazolási mechanizmus</span><span class="sxs-lookup"><span data-stu-id="239df-123">Attestation Mechanism.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAttestationMechanismType
Parameter Sets: (All)
Aliases:
Accepted values: None, Tpm, X509, SymmetricKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="239df-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="239df-124">-DefaultProfile</span></span>
<span data-ttu-id="239df-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="239df-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="239df-126">– Kívánt</span><span class="sxs-lookup"><span data-stu-id="239df-126">-Desired</span></span>
<span data-ttu-id="239df-127">Kezdeti dupla kívánt tulajdonságok.</span><span class="sxs-lookup"><span data-stu-id="239df-127">Initial twin desired properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="239df-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="239df-128">-DpsName</span></span>
<span data-ttu-id="239df-129">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="239df-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="239df-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="239df-130">-DpsObject</span></span>
<span data-ttu-id="239df-131">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="239df-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="239df-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="239df-132">-EdgeEnabled</span></span>
<span data-ttu-id="239df-133">Megjelölés az Edge engedélyezésével</span><span class="sxs-lookup"><span data-stu-id="239df-133">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="239df-134">-IotHub</span><span class="sxs-lookup"><span data-stu-id="239df-134">-IotHub</span></span>
<span data-ttu-id="239df-135">A cél IoT-hub állomásnevét tároló neve.</span><span class="sxs-lookup"><span data-stu-id="239df-135">Host name of target IoT Hub.</span></span>
<span data-ttu-id="239df-136">Szóközzel tagolt lista használata több IoT-hub esetében.</span><span class="sxs-lookup"><span data-stu-id="239df-136">Use space-separated list for multiple IoT Hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="239df-137">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="239df-137">-IotHubHostName</span></span>
<span data-ttu-id="239df-138">A cél IoT-hub állomásneve.</span><span class="sxs-lookup"><span data-stu-id="239df-138">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="239df-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="239df-139">-Name</span></span>
<span data-ttu-id="239df-140">A beiratkozási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="239df-140">Name of the enrollment group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="239df-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="239df-141">-PrimaryCAName</span></span>
<span data-ttu-id="239df-142">Az elsődleges legfelső szintű HITELESÍTÉSSZOLGÁLTATÓI tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="239df-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="239df-143">Ha a legfelső szintű HITELESÍTÉSSZOLGÁLTATÓI tanúsítványra vonatkozó tanúsítvány szükséges, akkor a legfelső szintű hitelesítésszolgáltatói nevet kell megadni.</span><span class="sxs-lookup"><span data-stu-id="239df-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="239df-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="239df-144">-PrimaryCertificate</span></span>
<span data-ttu-id="239df-145">Az elsődleges tanúsítványt tartalmazó fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="239df-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="239df-146">A X509. cer fájl vagy a. PEM fájl elérési útjának a 64-beli megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="239df-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="239df-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="239df-147">-PrimaryKey</span></span>
<span data-ttu-id="239df-148">Az elsődleges szimmetrikus megosztott elérési kulcs Base64 formátumban tárolva.</span><span class="sxs-lookup"><span data-stu-id="239df-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="239df-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="239df-149">-ProvisioningStatus</span></span>
<span data-ttu-id="239df-150">A beiratkozási bejegyzés engedélyezése és letiltása</span><span class="sxs-lookup"><span data-stu-id="239df-150">Enable or disable enrollment entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="239df-151">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="239df-151">-ReprovisionPolicy</span></span>
<span data-ttu-id="239df-152">Az eszközöknek a különböző IOT-hub-ra való ismételt kiépítéshez való ismételt kiépítésekor kezelendő adatforgalom.</span><span class="sxs-lookup"><span data-stu-id="239df-152">Device data to be handled on re-provision to different Iot Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSReprovisionType
Parameter Sets: (All)
Aliases:
Accepted values: reprovisionandmigratedata, reprovisionandresetdata, never

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="239df-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="239df-153">-ResourceGroupName</span></span>
<span data-ttu-id="239df-154">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="239df-154">Name of the Resource Group</span></span>

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

### <span data-ttu-id="239df-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="239df-155">-ResourceId</span></span>
<span data-ttu-id="239df-156">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="239df-156">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="239df-157">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="239df-157">-RootCertificate</span></span>
<span data-ttu-id="239df-158">Lehetővé teszi a X509attestation a legfelső szintű tanúsítványokkal való létrehozásban.</span><span class="sxs-lookup"><span data-stu-id="239df-158">Allows to create X509attestation using root certificates.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="239df-159">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="239df-159">-SecondaryCAName</span></span>
<span data-ttu-id="239df-160">A másodlagos legfelső szintű HITELESÍTÉSSZOLGÁLTATÓI tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="239df-160">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="239df-161">Ha a legfelső szintű HITELESÍTÉSSZOLGÁLTATÓI tanúsítványra vonatkozó tanúsítvány szükséges, akkor a legfelső szintű hitelesítésszolgáltatói nevet kell megadni.</span><span class="sxs-lookup"><span data-stu-id="239df-161">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="239df-162">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="239df-162">-SecondaryCertificate</span></span>
<span data-ttu-id="239df-163">A másodlagos tanúsítványt tartalmazó fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="239df-163">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="239df-164">A X509. cer fájl vagy a. PEM fájl elérési útjának a 64-beli megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="239df-164">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="239df-165">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="239df-165">-SecondaryKey</span></span>
<span data-ttu-id="239df-166">A másodlagos szimmetrikus megosztott elérési kulcs Base64 formátumban tárolva.</span><span class="sxs-lookup"><span data-stu-id="239df-166">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="239df-167">-Címke</span><span class="sxs-lookup"><span data-stu-id="239df-167">-Tag</span></span>
<span data-ttu-id="239df-168">Első Twin-Címkék</span><span class="sxs-lookup"><span data-stu-id="239df-168">Initial twin tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="239df-169">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="239df-169">-WebhookUrl</span></span>
<span data-ttu-id="239df-170">Az egyéni hozzárendelés-kérelmekhez használt webhorog URL-címe.</span><span class="sxs-lookup"><span data-stu-id="239df-170">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="239df-171">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="239df-171">-Confirm</span></span>
<span data-ttu-id="239df-172">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="239df-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="239df-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="239df-173">-WhatIf</span></span>
<span data-ttu-id="239df-174">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="239df-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="239df-175">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="239df-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="239df-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="239df-176">CommonParameters</span></span>
<span data-ttu-id="239df-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="239df-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="239df-178">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="239df-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="239df-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="239df-179">INPUTS</span></span>

### <span data-ttu-id="239df-180">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="239df-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="239df-181">System. String</span><span class="sxs-lookup"><span data-stu-id="239df-181">System.String</span></span>

## <span data-ttu-id="239df-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="239df-182">OUTPUTS</span></span>

### <span data-ttu-id="239df-183">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="239df-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="239df-184">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="239df-184">NOTES</span></span>

## <span data-ttu-id="239df-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="239df-185">RELATED LINKS</span></span>
