---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2563898E-C4A0-4530-AB46-30A6FC1BE55C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d295e2198cdbd8168d76b1f8e19e75fb4a662116
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015895"
---
# <span data-ttu-id="360ef-101">New-AzureServiceRemoteDesktopExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="360ef-101">New-AzureServiceRemoteDesktopExtensionConfig</span></span>

## <span data-ttu-id="360ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="360ef-102">SYNOPSIS</span></span>
<span data-ttu-id="360ef-103">Távoli asztali bővítmény konfigurációját hozza létre a központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="360ef-103">Generates a remote desktop extension configuration for a deployment.</span></span>

## <span data-ttu-id="360ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="360ef-104">SYNTAX</span></span>

### <span data-ttu-id="360ef-105">NewExtension (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="360ef-105">NewExtension (Default)</span></span>
```
New-AzureServiceRemoteDesktopExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential> [[-Expiration] <DateTime>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="360ef-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="360ef-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceRemoteDesktopExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential> [[-Expiration] <DateTime>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="360ef-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="360ef-107">DESCRIPTION</span></span>
<span data-ttu-id="360ef-108">A **New-AzureServiceRemoteDesktopExtensionConfig** parancsmag létrehoz egy konfigurációt egy távoli asztali bővítményhez a központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="360ef-108">The **New-AzureServiceRemoteDesktopExtensionConfig** cmdlet generates a configuration for a remote desktop extension for a deployment.</span></span>

## <span data-ttu-id="360ef-109">Példák</span><span class="sxs-lookup"><span data-stu-id="360ef-109">EXAMPLES</span></span>

### <span data-ttu-id="360ef-110">1. példa: távoli asztali bővítmény-konfiguráció létrehozása</span><span class="sxs-lookup"><span data-stu-id="360ef-110">Example 1: Generate a remote desktop extension configuration</span></span>
```
PS C:\> $rdpConfig = New-AzureServiceRemoteDesktopExtensionConfig -Credential $cred
```

<span data-ttu-id="360ef-111">A parancs a megadott hitelesítő adatokhoz létrehoz egy távoli asztali bővítmény-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="360ef-111">This command generates a remote desktop extension configuration for the specified credentials.</span></span>

### <span data-ttu-id="360ef-112">2. példa: a távoli asztali bővítmény konfigurációjának létrehozása meghatározott szerepkörhöz</span><span class="sxs-lookup"><span data-stu-id="360ef-112">Example 2: Generate a remote desktop extension configuration for a specified role</span></span>
```
PS C:\> $rdpConfig = New-AzureServiceRemoteDesktopExtensionConfig -Credential $cred -Role "WebRole01"
```

<span data-ttu-id="360ef-113">A parancs a megadott hitelesítő adatok és a WebRole01 szerepkör távoli asztali bővítmény-konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="360ef-113">This command generates a remote desktop extension configuration for the specified credentials and the WebRole01 role.</span></span>

## <span data-ttu-id="360ef-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="360ef-114">PARAMETERS</span></span>

### <span data-ttu-id="360ef-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="360ef-115">-CertificateThumbprint</span></span>
<span data-ttu-id="360ef-116">A magánjellegű konfiguráció titkosításához használt tanúsítvány-ujjlenyomatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="360ef-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="360ef-117">Ez a tanúsítvány már létezik a tanúsítványtárolóban.</span><span class="sxs-lookup"><span data-stu-id="360ef-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="360ef-118">Ha nem ad meg tanúsítványt, a parancsmag létrehoz egy tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="360ef-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="360ef-119">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="360ef-119">-Credential</span></span>
<span data-ttu-id="360ef-120">Adja meg a távoli asztalhoz engedélyezni kívánt hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="360ef-120">Specifies the credentials to enable for remote desktop.</span></span>
<span data-ttu-id="360ef-121">A hitelesítő adatok tartalmazzák a felhasználónevet és a jelszót.</span><span class="sxs-lookup"><span data-stu-id="360ef-121">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="360ef-122">-Lejárat</span><span class="sxs-lookup"><span data-stu-id="360ef-122">-Expiration</span></span>
<span data-ttu-id="360ef-123">Egy **datetime** típusú objektumot ad meg, amely lehetővé teszi, hogy a felhasználó megadhatja, hogy mikor jár le a felhasználói fiók.</span><span class="sxs-lookup"><span data-stu-id="360ef-123">Specifies a **DateTime** object that allows the user to specify when the user account expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="360ef-124">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="360ef-124">-ExtensionId</span></span>
<span data-ttu-id="360ef-125">A bővítmény AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="360ef-125">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="360ef-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="360ef-126">-InformationAction</span></span>
<span data-ttu-id="360ef-127">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="360ef-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="360ef-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="360ef-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="360ef-129">Folytassa</span><span class="sxs-lookup"><span data-stu-id="360ef-129">Continue</span></span>
- <span data-ttu-id="360ef-130">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="360ef-130">Ignore</span></span>
- <span data-ttu-id="360ef-131">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="360ef-131">Inquire</span></span>
- <span data-ttu-id="360ef-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="360ef-132">SilentlyContinue</span></span>
- <span data-ttu-id="360ef-133">állj</span><span class="sxs-lookup"><span data-stu-id="360ef-133">Stop</span></span>
- <span data-ttu-id="360ef-134">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="360ef-134">Suspend</span></span>

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

### <span data-ttu-id="360ef-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="360ef-135">-InformationVariable</span></span>
<span data-ttu-id="360ef-136">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="360ef-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="360ef-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="360ef-137">-Profile</span></span>
<span data-ttu-id="360ef-138">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="360ef-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="360ef-139">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="360ef-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="360ef-140">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="360ef-140">-Role</span></span>
<span data-ttu-id="360ef-141">Azt a választható szerepköröket adja meg, amelyekhez a távoli asztali konfigurációt meg szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="360ef-141">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="360ef-142">Ha ez a paraméter nincs megadva, a program az összes szerepkör alapértelmezett konfigurációjának megfelelően alkalmazza a távoli asztali konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="360ef-142">If this parameter is not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="360ef-143">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="360ef-143">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="360ef-144">Egy ujjlenyomat-ujjlenyomat-algoritmust ad meg, amely a tanúsítvány meghatározásához használt ujjlenyomatmal van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="360ef-144">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="360ef-145">Ez a paraméter nem kötelező, és az alapértelmezett érték az SHA1.</span><span class="sxs-lookup"><span data-stu-id="360ef-145">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="360ef-146">-Verzió</span><span class="sxs-lookup"><span data-stu-id="360ef-146">-Version</span></span>
<span data-ttu-id="360ef-147">A bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="360ef-147">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="360ef-148">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="360ef-148">-X509Certificate</span></span>
<span data-ttu-id="360ef-149">Itt adhatja meg azt a x509-tanúsítványt, amelyet a rendszer automatikusan feltölt a felhőalapú szolgáltatásba, és a privát konfiguráció titkosításához használja.</span><span class="sxs-lookup"><span data-stu-id="360ef-149">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: NewExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="360ef-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="360ef-150">CommonParameters</span></span>
<span data-ttu-id="360ef-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="360ef-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="360ef-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="360ef-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="360ef-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="360ef-153">INPUTS</span></span>

## <span data-ttu-id="360ef-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="360ef-154">OUTPUTS</span></span>

## <span data-ttu-id="360ef-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="360ef-155">NOTES</span></span>

## <span data-ttu-id="360ef-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="360ef-156">RELATED LINKS</span></span>

[<span data-ttu-id="360ef-157">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="360ef-157">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


