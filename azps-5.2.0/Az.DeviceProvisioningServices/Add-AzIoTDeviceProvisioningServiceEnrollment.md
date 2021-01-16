---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: b3c97abdee88615eedb2bb1f4452309326a4ebfa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328786"
---
# <span data-ttu-id="7379d-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="7379d-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="7379d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7379d-102">SYNOPSIS</span></span>
<span data-ttu-id="7379d-103">Hozzon létre egy eszközregisztrációs rekordot.</span><span class="sxs-lookup"><span data-stu-id="7379d-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="7379d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7379d-104">SYNTAX</span></span>

### <span data-ttu-id="7379d-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7379d-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> -AttestationType <PSAttestationMechanismType> [-DeviceId <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7379d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7379d-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> -AttestationType <PSAttestationMechanismType> [-DeviceId <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7379d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7379d-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 -AttestationType <PSAttestationMechanismType> [-DeviceId <String>] [-EndorsementKey <String>]
 [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7379d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7379d-108">DESCRIPTION</span></span>
<span data-ttu-id="7379d-109">Eszközbeiratkozást hozhat létre egy Azure IoT Hub-eszköz kiépítési szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="7379d-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="7379d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7379d-110">EXAMPLES</span></span>

### <span data-ttu-id="7379d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7379d-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="7379d-112">Regisztráció létrehozása Szimmetrikus kulcs tanúsítványtípussal</span><span class="sxs-lookup"><span data-stu-id="7379d-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="7379d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="7379d-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="7379d-114">Regisztráció létrehozása TPM-tanúsítványsal.</span><span class="sxs-lookup"><span data-stu-id="7379d-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="7379d-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="7379d-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="7379d-116">Regisztráció létrehozása X509-es tanúsítványtípussal</span><span class="sxs-lookup"><span data-stu-id="7379d-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="7379d-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="7379d-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="7379d-118">Hozzon létre egy regisztrációt Szimmetrikuskulcs típusú és kezdeti beállításállapotú tanúsítványokkal.</span><span class="sxs-lookup"><span data-stu-id="7379d-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="7379d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7379d-119">PARAMETERS</span></span>

### <span data-ttu-id="7379d-120">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="7379d-120">-AllocationPolicy</span></span>
<span data-ttu-id="7379d-121">A Központhoz rendelt eszköz kiosztásának típusa.</span><span class="sxs-lookup"><span data-stu-id="7379d-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="7379d-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7379d-122">-ApiVersion</span></span>
<span data-ttu-id="7379d-123">A kiépítési szolgáltatás API-verziója az egyéni hozzárendelési kérésben.</span><span class="sxs-lookup"><span data-stu-id="7379d-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="7379d-124">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="7379d-124">-AttestationType</span></span>
<span data-ttu-id="7379d-125">Igazolási mechanizmus.</span><span class="sxs-lookup"><span data-stu-id="7379d-125">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="7379d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7379d-126">-DefaultProfile</span></span>
<span data-ttu-id="7379d-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7379d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7379d-128">-Kívánt</span><span class="sxs-lookup"><span data-stu-id="7379d-128">-Desired</span></span>
<span data-ttu-id="7379d-129">A kezdeti kíván tulajdonságok.</span><span class="sxs-lookup"><span data-stu-id="7379d-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="7379d-130">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="7379d-130">-DeviceId</span></span>
<span data-ttu-id="7379d-131">IoT-központ eszközazonosítója.</span><span class="sxs-lookup"><span data-stu-id="7379d-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="7379d-132">-DpsName</span><span class="sxs-lookup"><span data-stu-id="7379d-132">-DpsName</span></span>
<span data-ttu-id="7379d-133">Az IoT-eszköz kiépítési szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="7379d-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7379d-134">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="7379d-134">-DpsObject</span></span>
<span data-ttu-id="7379d-135">IoT-eszköz kiépítési szolgáltatásobjektuma</span><span class="sxs-lookup"><span data-stu-id="7379d-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="7379d-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="7379d-136">-EdgeEnabled</span></span>
<span data-ttu-id="7379d-137">Flag indicating edge enablement.</span><span class="sxs-lookup"><span data-stu-id="7379d-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="7379d-138">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="7379d-138">-EndorsementKey</span></span>
<span data-ttu-id="7379d-139">TPM-támogató kulcs TPM-eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="7379d-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="7379d-140">-IotHub</span><span class="sxs-lookup"><span data-stu-id="7379d-140">-IotHub</span></span>
<span data-ttu-id="7379d-141">A cél IoT-központ állomásneve.</span><span class="sxs-lookup"><span data-stu-id="7379d-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="7379d-142">Több IoT-központhoz használjon térközt választó listát.</span><span class="sxs-lookup"><span data-stu-id="7379d-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="7379d-143">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="7379d-143">-IotHubHostName</span></span>
<span data-ttu-id="7379d-144">A cél IoT-központ állomásneve.</span><span class="sxs-lookup"><span data-stu-id="7379d-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="7379d-145">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="7379d-145">-PrimaryCAName</span></span>
<span data-ttu-id="7379d-146">Az elsődleges legfelső szintű hitelesítésszolgáltatói tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="7379d-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="7379d-147">Ha a legfelső szintű hitelesítésszolgáltatói tanúsítvánnyal való hitelesítést szeretné biztosítani, akkor meg kell adni egy legfelső szintű hitelesítésszolgáltató nevét.</span><span class="sxs-lookup"><span data-stu-id="7379d-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="7379d-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="7379d-148">-PrimaryCertificate</span></span>
<span data-ttu-id="7379d-149">Az elsődleges tanúsítványt tartalmazó fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="7379d-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="7379d-150">Az X509-es tanúsítvány .cer fájl vagy .pem fájl elérési útvonalának 64-es alapformátumú reprezentációja.</span><span class="sxs-lookup"><span data-stu-id="7379d-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="7379d-151">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="7379d-151">-PrimaryKey</span></span>
<span data-ttu-id="7379d-152">A base64 formátumban tárolt elsődleges szimmetrikus megosztott hozzáférési kulcs.</span><span class="sxs-lookup"><span data-stu-id="7379d-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="7379d-153">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="7379d-153">-ProvisioningStatus</span></span>
<span data-ttu-id="7379d-154">A regisztrációs bejegyzés engedélyezése vagy letiltása.</span><span class="sxs-lookup"><span data-stu-id="7379d-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="7379d-155">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="7379d-155">-RegistrationId</span></span>
<span data-ttu-id="7379d-156">Egyéni regisztrációs azonosító.</span><span class="sxs-lookup"><span data-stu-id="7379d-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="7379d-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="7379d-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="7379d-158">A másik Iot-központba való újraépítéssel kezelni szükséges eszközadatok.</span><span class="sxs-lookup"><span data-stu-id="7379d-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="7379d-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7379d-159">-ResourceGroupName</span></span>
<span data-ttu-id="7379d-160">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7379d-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7379d-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7379d-161">-ResourceId</span></span>
<span data-ttu-id="7379d-162">IoT-eszköz kiépítési szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="7379d-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="7379d-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="7379d-163">-RootCertificate</span></span>
<span data-ttu-id="7379d-164">Főtanúsítványok használatával X509atte-tanúsítványt hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="7379d-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="7379d-165">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="7379d-165">-SecondaryCAName</span></span>
<span data-ttu-id="7379d-166">A másodlagos legfelső szintű hitelesítésszolgáltatói tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="7379d-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="7379d-167">Ha a legfelső szintű hitelesítésszolgáltatói tanúsítvánnyal való hitelesítést szeretné biztosítani, akkor meg kell adni egy legfelső szintű hitelesítésszolgáltató nevét.</span><span class="sxs-lookup"><span data-stu-id="7379d-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="7379d-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="7379d-168">-SecondaryCertificate</span></span>
<span data-ttu-id="7379d-169">A másodlagos tanúsítványt tartalmazó fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="7379d-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="7379d-170">Az X509-es tanúsítvány .cer fájl vagy .pem fájl elérési útvonalának 64-es alapformátumú reprezentációja.</span><span class="sxs-lookup"><span data-stu-id="7379d-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="7379d-171">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="7379d-171">-SecondaryKey</span></span>
<span data-ttu-id="7379d-172">A másodlagos szimmetrikus megosztott hozzáférési kulcs, amely base64 formátumban van tárolva.</span><span class="sxs-lookup"><span data-stu-id="7379d-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="7379d-173">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="7379d-173">-StorageRootKey</span></span>
<span data-ttu-id="7379d-174">TPM-eszköz TPM-tárterületének gyökérkulcsa.</span><span class="sxs-lookup"><span data-stu-id="7379d-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="7379d-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="7379d-175">-Tag</span></span>
<span data-ttu-id="7379d-176">Kezdeti címkecímkék.</span><span class="sxs-lookup"><span data-stu-id="7379d-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="7379d-177">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="7379d-177">-WebhookUrl</span></span>
<span data-ttu-id="7379d-178">Az egyéni hozzárendelési kérések webhook URL-címe.</span><span class="sxs-lookup"><span data-stu-id="7379d-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="7379d-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7379d-179">-Confirm</span></span>
<span data-ttu-id="7379d-180">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7379d-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7379d-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7379d-181">-WhatIf</span></span>
<span data-ttu-id="7379d-182">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7379d-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7379d-183">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7379d-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7379d-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7379d-184">CommonParameters</span></span>
<span data-ttu-id="7379d-185">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7379d-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7379d-186">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7379d-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7379d-187">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7379d-187">INPUTS</span></span>

### <span data-ttu-id="7379d-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="7379d-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="7379d-189">System.String</span><span class="sxs-lookup"><span data-stu-id="7379d-189">System.String</span></span>

## <span data-ttu-id="7379d-190">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7379d-190">OUTPUTS</span></span>

### <span data-ttu-id="7379d-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="7379d-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="7379d-192">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7379d-192">NOTES</span></span>

## <span data-ttu-id="7379d-193">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7379d-193">RELATED LINKS</span></span>
