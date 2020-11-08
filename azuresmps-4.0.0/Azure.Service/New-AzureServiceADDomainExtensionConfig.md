---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: DFD4BA63-A7DE-49DD-878C-68062EF17873
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d4830d049ab01142c75847b4afd5419729f14d1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015897"
---
# <span data-ttu-id="2104c-101">New-AzureServiceADDomainExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="2104c-101">New-AzureServiceADDomainExtensionConfig</span></span>

## <span data-ttu-id="2104c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2104c-102">SYNOPSIS</span></span>
<span data-ttu-id="2104c-103">A Felhőbeli szolgáltatások AD domain-bővítményének konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="2104c-103">Generates the configuration for the AD domain extension for cloud services.</span></span>

## <span data-ttu-id="2104c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2104c-104">SYNTAX</span></span>

### <span data-ttu-id="2104c-105">JoinDomainUsingEnumOptions (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2104c-105">JoinDomainUsingEnumOptions (Default)</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>] [[-OUPath] <String>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2104c-106">JoinDomainUsingJoinOption</span><span class="sxs-lookup"><span data-stu-id="2104c-106">JoinDomainUsingJoinOption</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32> [[-OUPath] <String>] [[-Version] <String>]
 [[-ExtensionId] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2104c-107">WorkGroupName</span><span class="sxs-lookup"><span data-stu-id="2104c-107">WorkGroupName</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2104c-108">JoinDomainUsingEnumOptionsAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="2104c-108">JoinDomainUsingEnumOptionsAndThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>] [[-OUPath] <String>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2104c-109">JoinDomainUsingJoinOptionAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="2104c-109">JoinDomainUsingJoinOptionAndThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32> [[-OUPath] <String>] [[-Version] <String>]
 [[-ExtensionId] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2104c-110">WorkGroupNameThumbprint</span><span class="sxs-lookup"><span data-stu-id="2104c-110">WorkGroupNameThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2104c-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="2104c-111">DESCRIPTION</span></span>
<span data-ttu-id="2104c-112">A **New-AzureServiceADDomainExtensionConfig** parancsmag a felhőalapú szolgáltatások Active Directory-bővítményének konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="2104c-112">The **New-AzureServiceADDomainExtensionConfig** cmdlet generates the configuration for the Active Directory (AD) domain extension for cloud services.</span></span>

## <span data-ttu-id="2104c-113">Példák</span><span class="sxs-lookup"><span data-stu-id="2104c-113">EXAMPLES</span></span>

### <span data-ttu-id="2104c-114">Példa 1: AD domain-konfiguráció megadása</span><span class="sxs-lookup"><span data-stu-id="2104c-114">Example 1: Specify an AD domain configuration</span></span>
```
PS C:\> $ExtensionCfg = New-AzureServiceADDomainExtensionConfig -Role WorkerRole1 -DomainName $Domain -Credential $Cred -JoinOption 35;

PS C:\> New-AzureDeployment -ServiceName $CloudSvc -Slot "Production" -Package $Pkg -Configuration $Config -ExtensionConfiguration $ExtensionCfg;
```

<span data-ttu-id="2104c-115">A parancs létrehozza az AD domain bővítmény konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="2104c-115">This command generates a configuration for the AD domain extension.</span></span>

## <span data-ttu-id="2104c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2104c-116">PARAMETERS</span></span>

### <span data-ttu-id="2104c-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="2104c-117">-CertificateThumbprint</span></span>
<span data-ttu-id="2104c-118">A magánjellegű konfiguráció titkosításához használt tanúsítvány-ujjlenyomatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="2104c-118">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="2104c-119">Ez a tanúsítvány már létezik a tanúsítványtárolóban.</span><span class="sxs-lookup"><span data-stu-id="2104c-119">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="2104c-120">Ha nem ad meg tanúsítványt, a parancsmag létrehoz egy tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="2104c-120">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2104c-121">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="2104c-121">-Credential</span></span>
<span data-ttu-id="2104c-122">Megadja a AD-tartományhoz való csatlakozáshoz használt hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="2104c-122">Specifies the credentials to use to join the AD domain.</span></span>
<span data-ttu-id="2104c-123">A hitelesítő adatok tartalmazzák a felhasználónevet és a jelszót.</span><span class="sxs-lookup"><span data-stu-id="2104c-123">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2104c-124">-Tartománynév</span><span class="sxs-lookup"><span data-stu-id="2104c-124">-DomainName</span></span>
<span data-ttu-id="2104c-125">Az AD tartománynevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="2104c-125">Specifies the AD domain name.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2104c-126">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="2104c-126">-ExtensionId</span></span>
<span data-ttu-id="2104c-127">A bővítmény AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2104c-127">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2104c-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2104c-128">-InformationAction</span></span>
<span data-ttu-id="2104c-129">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="2104c-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2104c-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2104c-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2104c-131">Folytassa</span><span class="sxs-lookup"><span data-stu-id="2104c-131">Continue</span></span>
- <span data-ttu-id="2104c-132">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="2104c-132">Ignore</span></span>
- <span data-ttu-id="2104c-133">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="2104c-133">Inquire</span></span>
- <span data-ttu-id="2104c-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2104c-134">SilentlyContinue</span></span>
- <span data-ttu-id="2104c-135">állj</span><span class="sxs-lookup"><span data-stu-id="2104c-135">Stop</span></span>
- <span data-ttu-id="2104c-136">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="2104c-136">Suspend</span></span>

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

### <span data-ttu-id="2104c-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2104c-137">-InformationVariable</span></span>
<span data-ttu-id="2104c-138">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="2104c-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2104c-139">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="2104c-139">-JoinOption</span></span>
<span data-ttu-id="2104c-140">A bekapcsolódási beállítás enumerálása.</span><span class="sxs-lookup"><span data-stu-id="2104c-140">Specifies the join option enumeration.</span></span>

```yaml
Type: UInt32
Parameter Sets: JoinDomainUsingJoinOption, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2104c-141">– Beállítások</span><span class="sxs-lookup"><span data-stu-id="2104c-141">-Options</span></span>
<span data-ttu-id="2104c-142">A jelöletlen egész szám illesztési lehetőséget adja meg.</span><span class="sxs-lookup"><span data-stu-id="2104c-142">Specifies the unsigned integer join option.</span></span>

```yaml
Type: JoinOptions
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingEnumOptionsAndThumbprint
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2104c-143">-OUPath</span><span class="sxs-lookup"><span data-stu-id="2104c-143">-OUPath</span></span>
<span data-ttu-id="2104c-144">A szervezeti egység (OU) elérési útját adja meg az AD-tartományhoz való csatlakozás művelethez.</span><span class="sxs-lookup"><span data-stu-id="2104c-144">Specifies the organization unit (OU) path for AD domain join operation.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2104c-145">-Profil</span><span class="sxs-lookup"><span data-stu-id="2104c-145">-Profile</span></span>
<span data-ttu-id="2104c-146">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="2104c-146">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2104c-147">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="2104c-147">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2104c-148">– Újraindítás</span><span class="sxs-lookup"><span data-stu-id="2104c-148">-Restart</span></span>
<span data-ttu-id="2104c-149">Azt adja meg, hogy az illesztési művelet sikeres-e a számítógép újraindításával.</span><span class="sxs-lookup"><span data-stu-id="2104c-149">Specifies whether to restart the computer if the join operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2104c-150">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="2104c-150">-Role</span></span>
<span data-ttu-id="2104c-151">A szerepkörök választható tömböket adja meg az AD-tartomány távoli asztali konfigurációjának megadásához.</span><span class="sxs-lookup"><span data-stu-id="2104c-151">Specifies an optional array of roles to specify the remote desktop configuration for the AD domain configuration.</span></span>
<span data-ttu-id="2104c-152">Ha nem adja meg ezt a paramétert, akkor a rendszer minden szerepkör esetében az alapértelmezett konfigurációként alkalmazza az AD tartomány konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="2104c-152">If you do not specify this parameter, the AD domain configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2104c-153">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="2104c-153">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="2104c-154">A tanúsítvány meghatározására szolgáló ujjlenyomat-algoritmust ad meg.</span><span class="sxs-lookup"><span data-stu-id="2104c-154">Specifies a thumbprint hashing algorithm that is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="2104c-155">Ez a paraméter nem kötelező, és az alapértelmezett érték az SHA1.</span><span class="sxs-lookup"><span data-stu-id="2104c-155">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2104c-156">-UnjoinDomainCredential</span><span class="sxs-lookup"><span data-stu-id="2104c-156">-UnjoinDomainCredential</span></span>
<span data-ttu-id="2104c-157">Megadja a hitelesítő adatokat (Felhasználónév és jelszó) a AD-tartomány kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="2104c-157">Specifies the credentials (user name and password) to unjoin the AD domain.</span></span>

```yaml
Type: PSCredential
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2104c-158">-Verzió</span><span class="sxs-lookup"><span data-stu-id="2104c-158">-Version</span></span>
<span data-ttu-id="2104c-159">A bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2104c-159">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2104c-160">-WorkgroupName</span><span class="sxs-lookup"><span data-stu-id="2104c-160">-WorkgroupName</span></span>
<span data-ttu-id="2104c-161">A munkacsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2104c-161">Specifies the workgroup name.</span></span>

```yaml
Type: String
Parameter Sets: WorkGroupName, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2104c-162">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="2104c-162">-X509Certificate</span></span>
<span data-ttu-id="2104c-163">Itt adhatja meg azt az X. 509 tanúsítványt, amelyet a rendszer automatikusan feltölt a felhőalapú szolgáltatásba, és a privát konfiguráció titkosítására szolgál.</span><span class="sxs-lookup"><span data-stu-id="2104c-163">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, WorkGroupName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2104c-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2104c-164">CommonParameters</span></span>
<span data-ttu-id="2104c-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2104c-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2104c-166">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2104c-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2104c-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2104c-167">INPUTS</span></span>

## <span data-ttu-id="2104c-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2104c-168">OUTPUTS</span></span>

## <span data-ttu-id="2104c-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2104c-169">NOTES</span></span>

## <span data-ttu-id="2104c-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2104c-170">RELATED LINKS</span></span>

[<span data-ttu-id="2104c-171">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="2104c-171">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="2104c-172">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="2104c-172">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


