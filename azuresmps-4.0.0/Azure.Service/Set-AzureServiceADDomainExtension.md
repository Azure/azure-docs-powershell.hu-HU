---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 350638E1-636E-484B-88EB-91F48129D80B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c665288d12897e4ab7277dd4ccf4bc5d975c037
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016048"
---
# <span data-ttu-id="b2648-101">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="b2648-101">Set-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="b2648-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2648-102">SYNOPSIS</span></span>
<span data-ttu-id="b2648-103">Engedélyezi az AD domain-bővítményt egy felhőalapú szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="b2648-103">Enables an AD Domain extension for a cloud service.</span></span>

## <span data-ttu-id="b2648-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2648-104">SYNTAX</span></span>

### <span data-ttu-id="b2648-105">JoinDomainUsingEnumOptions (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b2648-105">JoinDomainUsingEnumOptions (Default)</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>]
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b2648-106">JoinDomainUsingJoinOption</span><span class="sxs-lookup"><span data-stu-id="b2648-106">JoinDomainUsingJoinOption</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32>
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b2648-107">WorkGroupName</span><span class="sxs-lookup"><span data-stu-id="b2648-107">WorkGroupName</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b2648-108">JoinDomainUsingEnumOptionsAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="b2648-108">JoinDomainUsingEnumOptionsAndThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>]
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b2648-109">JoinDomainUsingJoinOptionAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="b2648-109">JoinDomainUsingJoinOptionAndThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32>
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b2648-110">WorkGroupNameThumbprint</span><span class="sxs-lookup"><span data-stu-id="b2648-110">WorkGroupNameThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b2648-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2648-111">DESCRIPTION</span></span>
<span data-ttu-id="b2648-112">A **set-AzureServiceADDomainExtension** parancsmag ad (Active Directory) tartományi bővítményt engedélyez a felhőalapú szolgáltatásokhoz.</span><span class="sxs-lookup"><span data-stu-id="b2648-112">The **Set-AzureServiceADDomainExtension** cmdlet enables an AD (Active Directory) Domain extension for a cloud service.</span></span>

## <span data-ttu-id="b2648-113">Példák</span><span class="sxs-lookup"><span data-stu-id="b2648-113">EXAMPLES</span></span>

### <span data-ttu-id="b2648-114">1:</span><span class="sxs-lookup"><span data-stu-id="b2648-114">1:</span></span>
```

```

## <span data-ttu-id="b2648-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2648-115">PARAMETERS</span></span>

### <span data-ttu-id="b2648-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="b2648-116">-CertificateThumbprint</span></span>
<span data-ttu-id="b2648-117">A magánjellegű konfiguráció titkosításához használt tanúsítvány-ujjlenyomatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2648-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="b2648-118">Ez a tanúsítvány már létezik a tanúsítványtárolóban.</span><span class="sxs-lookup"><span data-stu-id="b2648-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="b2648-119">Ha nem ad meg tanúsítványt, a parancsmag létrehoz egy tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="b2648-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2648-120">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="b2648-120">-Credential</span></span>
<span data-ttu-id="b2648-121">Megadja a AD-tartományhoz való csatlakozáshoz szükséges hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="b2648-121">Specifies the credentials to join the AD domain.</span></span>
<span data-ttu-id="b2648-122">A hitelesítő adatok tartalmazzák a felhasználónevet és a jelszót.</span><span class="sxs-lookup"><span data-stu-id="b2648-122">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2648-123">-Tartománynév</span><span class="sxs-lookup"><span data-stu-id="b2648-123">-DomainName</span></span>
<span data-ttu-id="b2648-124">Az AD tartománynevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2648-124">Specifies the AD domain name.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2648-125">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="b2648-125">-ExtensionId</span></span>
<span data-ttu-id="b2648-126">A bővítmény AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2648-126">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2648-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b2648-127">-InformationAction</span></span>
<span data-ttu-id="b2648-128">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="b2648-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b2648-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b2648-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b2648-130">Folytassa</span><span class="sxs-lookup"><span data-stu-id="b2648-130">Continue</span></span>
- <span data-ttu-id="b2648-131">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="b2648-131">Ignore</span></span>
- <span data-ttu-id="b2648-132">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="b2648-132">Inquire</span></span>
- <span data-ttu-id="b2648-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b2648-133">SilentlyContinue</span></span>
- <span data-ttu-id="b2648-134">állj</span><span class="sxs-lookup"><span data-stu-id="b2648-134">Stop</span></span>
- <span data-ttu-id="b2648-135">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="b2648-135">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2648-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b2648-136">-InformationVariable</span></span>
<span data-ttu-id="b2648-137">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="b2648-137">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2648-138">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="b2648-138">-JoinOption</span></span>
<span data-ttu-id="b2648-139">A bekapcsolódási beállítás enumerálása.</span><span class="sxs-lookup"><span data-stu-id="b2648-139">Specifies the join option enumeration.</span></span>

```yaml
Type: UInt32
Parameter Sets: JoinDomainUsingJoinOption, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2648-140">– Beállítások</span><span class="sxs-lookup"><span data-stu-id="b2648-140">-Options</span></span>
<span data-ttu-id="b2648-141">A jelöletlen egész szám illesztési lehetőséget adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2648-141">Specifies the unsigned integer join option.</span></span>

```yaml
Type: JoinOptions
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingEnumOptionsAndThumbprint
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2648-142">-OUPath</span><span class="sxs-lookup"><span data-stu-id="b2648-142">-OUPath</span></span>
<span data-ttu-id="b2648-143">Itt adhatja meg a szervezeti egység (OU) elérési útját az AD-tartomány csatlakozási műveletéhez.</span><span class="sxs-lookup"><span data-stu-id="b2648-143">Specifies the Organization Unit (OU) path for the AD domain join operation.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2648-144">-Profil</span><span class="sxs-lookup"><span data-stu-id="b2648-144">-Profile</span></span>
<span data-ttu-id="b2648-145">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b2648-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b2648-146">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b2648-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2648-147">– Újraindítás</span><span class="sxs-lookup"><span data-stu-id="b2648-147">-Restart</span></span>
<span data-ttu-id="b2648-148">Azt adja meg, hogy az illesztési művelet sikeres-e a számítógép újraindításával.</span><span class="sxs-lookup"><span data-stu-id="b2648-148">Specifies whether to restart the computer if the join operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2648-149">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="b2648-149">-Role</span></span>
<span data-ttu-id="b2648-150">Azt a választható szerepköröket adja meg, amelyekhez a távoli asztali konfigurációt meg szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="b2648-150">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="b2648-151">Ha nincs megadva, az Active Directory tartományi konfiguráció alapértelmezés szerint az összes szerepkör alapértelmezett konfigurációjának van megadva.</span><span class="sxs-lookup"><span data-stu-id="b2648-151">If not specified the AD domain configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2648-152">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="b2648-152">-ServiceName</span></span>
<span data-ttu-id="b2648-153">A felhőalapú szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2648-153">Specifies the cloud service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2648-154">-Slot</span><span class="sxs-lookup"><span data-stu-id="b2648-154">-Slot</span></span>
<span data-ttu-id="b2648-155">A módosítani kívánt központi verzió környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2648-155">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="b2648-156">A paraméter elfogadható értékei a következők: termelés vagy megállóhely.</span><span class="sxs-lookup"><span data-stu-id="b2648-156">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2648-157">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="b2648-157">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="b2648-158">Egy ujjlenyomat-ujjlenyomat-algoritmust ad meg, amely a tanúsítvány meghatározásához használt ujjlenyomatmal van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="b2648-158">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="b2648-159">Ez a paraméter nem kötelező, és az alapértelmezett érték az SHA1.</span><span class="sxs-lookup"><span data-stu-id="b2648-159">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2648-160">-UnjoinDomainCredential</span><span class="sxs-lookup"><span data-stu-id="b2648-160">-UnjoinDomainCredential</span></span>
<span data-ttu-id="b2648-161">Megadja a hitelesítő adatokat (Felhasználónév és jelszó) a AD-tartomány kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="b2648-161">Specifies the credentials (user name and password) to unjoin the AD domain.</span></span>

```yaml
Type: PSCredential
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2648-162">-Verzió</span><span class="sxs-lookup"><span data-stu-id="b2648-162">-Version</span></span>
<span data-ttu-id="b2648-163">A bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2648-163">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2648-164">-WorkgroupName</span><span class="sxs-lookup"><span data-stu-id="b2648-164">-WorkgroupName</span></span>
<span data-ttu-id="b2648-165">A munkacsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2648-165">Specifies the workgroup name.</span></span>

```yaml
Type: String
Parameter Sets: WorkGroupName, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2648-166">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="b2648-166">-X509Certificate</span></span>
<span data-ttu-id="b2648-167">Itt adhatja meg azt a x509-tanúsítványt, amelyet a rendszer automatikusan feltölt a felhőalapú szolgáltatásba, és a privát konfiguráció titkosításához használja.</span><span class="sxs-lookup"><span data-stu-id="b2648-167">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, WorkGroupName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2648-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2648-168">CommonParameters</span></span>
<span data-ttu-id="b2648-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2648-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2648-170">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2648-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2648-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2648-171">INPUTS</span></span>

## <span data-ttu-id="b2648-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2648-172">OUTPUTS</span></span>

## <span data-ttu-id="b2648-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2648-173">NOTES</span></span>

## <span data-ttu-id="b2648-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2648-174">RELATED LINKS</span></span>

[<span data-ttu-id="b2648-175">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="b2648-175">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="b2648-176">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="b2648-176">Remove-AzureServiceADDomainExtension</span></span>](./Remove-AzureServiceADDomainExtension.md)

[<span data-ttu-id="b2648-177">Új – AzureServiceADDomainExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="b2648-177">New-AzureServiceADDomainExtensionConfig</span></span>](./New-AzureServiceADDomainExtensionConfig.md)


