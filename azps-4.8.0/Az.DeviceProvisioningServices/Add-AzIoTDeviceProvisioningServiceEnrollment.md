---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: e02d9c1ca9a5d45f081f168c3d8736d502f52094
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182256"
---
# <span data-ttu-id="5f6a4-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="5f6a4-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="5f6a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5f6a4-102">SYNOPSIS</span></span>
<span data-ttu-id="5f6a4-103">Eszköz-beiktatási rekord létrehozása</span><span class="sxs-lookup"><span data-stu-id="5f6a4-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="5f6a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5f6a4-104">SYNTAX</span></span>

### <span data-ttu-id="5f6a4-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5f6a4-105">ResourceSet (Default)</span></span>
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

### <span data-ttu-id="5f6a4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5f6a4-106">InputObjectSet</span></span>
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

### <span data-ttu-id="5f6a4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5f6a4-107">ResourceIdSet</span></span>
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

## <span data-ttu-id="5f6a4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5f6a4-108">DESCRIPTION</span></span>
<span data-ttu-id="5f6a4-109">Eszköz-igénylés létrehozása Azure IoT hub eszközök kiépítési szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="5f6a4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5f6a4-110">EXAMPLES</span></span>

### <span data-ttu-id="5f6a4-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5f6a4-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="5f6a4-112">Tanúsítványigénylési típus SymmetricKey létrehozása</span><span class="sxs-lookup"><span data-stu-id="5f6a4-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="5f6a4-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="5f6a4-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="5f6a4-114">Tanúsítványigénylés létrehozása a TPM-tanúsítvánnyal.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="5f6a4-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="5f6a4-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="5f6a4-116">Tanúsítványigénylési típus X509 létrehozása</span><span class="sxs-lookup"><span data-stu-id="5f6a4-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="5f6a4-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="5f6a4-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag
```

<span data-ttu-id="5f6a4-118">Hozzon létre egy beiratkozási típust a SymmetricKey és a Initial Twin állammal.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="5f6a4-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5f6a4-119">PARAMETERS</span></span>

### <span data-ttu-id="5f6a4-120">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="5f6a4-120">-AllocationPolicy</span></span>
<span data-ttu-id="5f6a4-121">A hub-hoz rendelt eszközhöz tartozó kiosztás típusa.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="5f6a4-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5f6a4-122">-ApiVersion</span></span>
<span data-ttu-id="5f6a4-123">A kiépítési szolgáltatás API-változata az egyéni hozzárendelés-kérésben.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="5f6a4-124">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="5f6a4-124">-AttestationType</span></span>
<span data-ttu-id="5f6a4-125">Igazolási mechanizmus</span><span class="sxs-lookup"><span data-stu-id="5f6a4-125">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="5f6a4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f6a4-126">-DefaultProfile</span></span>
<span data-ttu-id="5f6a4-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f6a4-128">– Kívánt</span><span class="sxs-lookup"><span data-stu-id="5f6a4-128">-Desired</span></span>
<span data-ttu-id="5f6a4-129">Kezdeti dupla kívánt tulajdonságok.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="5f6a4-130">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="5f6a4-130">-DeviceId</span></span>
<span data-ttu-id="5f6a4-131">IoT hub-eszköz azonosítója</span><span class="sxs-lookup"><span data-stu-id="5f6a4-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="5f6a4-132">-DpsName</span><span class="sxs-lookup"><span data-stu-id="5f6a4-132">-DpsName</span></span>
<span data-ttu-id="5f6a4-133">A IoT-eszközök kiépítési szolgáltatásának neve</span><span class="sxs-lookup"><span data-stu-id="5f6a4-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5f6a4-134">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="5f6a4-134">-DpsObject</span></span>
<span data-ttu-id="5f6a4-135">IoT-eszköz kiépítési szolgáltatási objektuma</span><span class="sxs-lookup"><span data-stu-id="5f6a4-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="5f6a4-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="5f6a4-136">-EdgeEnabled</span></span>
<span data-ttu-id="5f6a4-137">Megjelölés az Edge engedélyezésével</span><span class="sxs-lookup"><span data-stu-id="5f6a4-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="5f6a4-138">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="5f6a4-138">-EndorsementKey</span></span>
<span data-ttu-id="5f6a4-139">TPM-eszköz TPM-záradékának kulcsa.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="5f6a4-140">-IotHub</span><span class="sxs-lookup"><span data-stu-id="5f6a4-140">-IotHub</span></span>
<span data-ttu-id="5f6a4-141">A cél IoT-hub állomásnevét tároló neve.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="5f6a4-142">Szóközzel tagolt lista használata több IoT-hub esetében.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="5f6a4-143">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="5f6a4-143">-IotHubHostName</span></span>
<span data-ttu-id="5f6a4-144">A cél IoT-hub állomásneve.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="5f6a4-145">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="5f6a4-145">-PrimaryCAName</span></span>
<span data-ttu-id="5f6a4-146">Az elsődleges legfelső szintű HITELESÍTÉSSZOLGÁLTATÓI tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="5f6a4-147">Ha a legfelső szintű HITELESÍTÉSSZOLGÁLTATÓI tanúsítványra vonatkozó tanúsítvány szükséges, akkor a legfelső szintű hitelesítésszolgáltatói nevet kell megadni.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="5f6a4-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="5f6a4-148">-PrimaryCertificate</span></span>
<span data-ttu-id="5f6a4-149">Az elsődleges tanúsítványt tartalmazó fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="5f6a4-150">A X509. cer fájl vagy a. PEM fájl elérési útjának a 64-beli megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="5f6a4-151">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="5f6a4-151">-PrimaryKey</span></span>
<span data-ttu-id="5f6a4-152">Az elsődleges szimmetrikus megosztott elérési kulcs Base64 formátumban tárolva.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="5f6a4-153">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="5f6a4-153">-ProvisioningStatus</span></span>
<span data-ttu-id="5f6a4-154">A beiratkozási bejegyzés engedélyezése és letiltása</span><span class="sxs-lookup"><span data-stu-id="5f6a4-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="5f6a4-155">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="5f6a4-155">-RegistrationId</span></span>
<span data-ttu-id="5f6a4-156">Egyéni beiratkozási regisztrációs azonosító</span><span class="sxs-lookup"><span data-stu-id="5f6a4-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="5f6a4-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="5f6a4-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="5f6a4-158">Az eszközöknek a különböző IOT-hub-ra való ismételt kiépítéshez való ismételt kiépítésekor kezelendő adatforgalom.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="5f6a4-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f6a4-159">-ResourceGroupName</span></span>
<span data-ttu-id="5f6a4-160">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5f6a4-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5f6a4-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f6a4-161">-ResourceId</span></span>
<span data-ttu-id="5f6a4-162">IoT eszközök kiépítési szolgáltatásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="5f6a4-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5f6a4-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="5f6a4-163">-RootCertificate</span></span>
<span data-ttu-id="5f6a4-164">Lehetővé teszi a X509attestation a legfelső szintű tanúsítványokkal való létrehozásban.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="5f6a4-165">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="5f6a4-165">-SecondaryCAName</span></span>
<span data-ttu-id="5f6a4-166">A másodlagos legfelső szintű HITELESÍTÉSSZOLGÁLTATÓI tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="5f6a4-167">Ha a legfelső szintű HITELESÍTÉSSZOLGÁLTATÓI tanúsítványra vonatkozó tanúsítvány szükséges, akkor a legfelső szintű hitelesítésszolgáltatói nevet kell megadni.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="5f6a4-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="5f6a4-168">-SecondaryCertificate</span></span>
<span data-ttu-id="5f6a4-169">A másodlagos tanúsítványt tartalmazó fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="5f6a4-170">A X509. cer fájl vagy a. PEM fájl elérési útjának a 64-beli megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="5f6a4-171">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="5f6a4-171">-SecondaryKey</span></span>
<span data-ttu-id="5f6a4-172">A másodlagos szimmetrikus megosztott elérési kulcs Base64 formátumban tárolva.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="5f6a4-173">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="5f6a4-173">-StorageRootKey</span></span>
<span data-ttu-id="5f6a4-174">TPM-tároló gyökérszintű kulcsa a TPM-eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="5f6a4-175">-Címke</span><span class="sxs-lookup"><span data-stu-id="5f6a4-175">-Tag</span></span>
<span data-ttu-id="5f6a4-176">Első Twin-Címkék</span><span class="sxs-lookup"><span data-stu-id="5f6a4-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="5f6a4-177">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="5f6a4-177">-WebhookUrl</span></span>
<span data-ttu-id="5f6a4-178">Az egyéni hozzárendelés-kérelmekhez használt webhorog URL-címe.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="5f6a4-179">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5f6a4-179">-Confirm</span></span>
<span data-ttu-id="5f6a4-180">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f6a4-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f6a4-181">-WhatIf</span></span>
<span data-ttu-id="5f6a4-182">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f6a4-183">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f6a4-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f6a4-184">CommonParameters</span></span>
<span data-ttu-id="5f6a4-185">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5f6a4-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f6a4-186">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f6a4-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f6a4-187">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f6a4-187">INPUTS</span></span>

### <span data-ttu-id="5f6a4-188">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="5f6a4-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="5f6a4-189">System. String</span><span class="sxs-lookup"><span data-stu-id="5f6a4-189">System.String</span></span>

## <span data-ttu-id="5f6a4-190">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f6a4-190">OUTPUTS</span></span>

### <span data-ttu-id="5f6a4-191">Microsoft. Azure. Command. Management. DeviceProvisioningServices. models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="5f6a4-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="5f6a4-192">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5f6a4-192">NOTES</span></span>

## <span data-ttu-id="5f6a4-193">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f6a4-193">RELATED LINKS</span></span>
