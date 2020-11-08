---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5C8B1482-80B0-4060-A35D-E9D394156886
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a6303e685ea02408772a237c6b5f154764107e4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015813"
---
# <span data-ttu-id="aa8a3-101">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="aa8a3-101">Set-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="aa8a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa8a3-102">SYNOPSIS</span></span>
<span data-ttu-id="aa8a3-103">Engedélyezi a távoli asztali bővítményt meghatározott szerepkör (ek) vagy az összes szerepkör egy telepített szolgáltatásban vagy a központi telepítésben.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-103">Enables remote desktop extension on specified role(s) or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="aa8a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa8a3-104">SYNTAX</span></span>

### <span data-ttu-id="aa8a3-105">SetExtension (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aa8a3-105">SetExtension (Default)</span></span>
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="aa8a3-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="aa8a3-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="aa8a3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa8a3-107">DESCRIPTION</span></span>
<span data-ttu-id="aa8a3-108">A **set-AzureServiceRemoteDesktopExtension** parancsmag a megadott szerepkörökre vagy a telepített szolgáltatásokban vagy a telepítéshez tartozó összes szerepkörre vonatkozóan engedélyezi a távoli asztali bővítményt.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-108">The **Set-AzureServiceRemoteDesktopExtension** cmdlet enables remote desktop extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="aa8a3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="aa8a3-109">EXAMPLES</span></span>

### <span data-ttu-id="aa8a3-110">1. példa: a távoli asztali bővítmény engedélyezése</span><span class="sxs-lookup"><span data-stu-id="aa8a3-110">Example 1: Enable remote desktop extension</span></span>
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds
```

<span data-ttu-id="aa8a3-111">Ez a parancs engedélyezi a megadott szolgáltatáshoz tartozó távoli asztali bővítményt.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-111">This command enables the remote desktop extension for the specified service.</span></span>

### <span data-ttu-id="aa8a3-112">2. példa: a távoli asztali bővítmény engedélyezése meghatározott szerepkörhöz</span><span class="sxs-lookup"><span data-stu-id="aa8a3-112">Example 2: Enable remote desktop extension for a specified role</span></span>
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds -Role "WebRole1"
```

<span data-ttu-id="aa8a3-113">Ez a parancs lehetővé teszi a megadott szolgáltatáshoz és szerepkörhöz tartozó távoli asztali bővítményt.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-113">This command enables the remote desktop extension for the specified service and role.</span></span>

## <span data-ttu-id="aa8a3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa8a3-114">PARAMETERS</span></span>

### <span data-ttu-id="aa8a3-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="aa8a3-115">-CertificateThumbprint</span></span>
<span data-ttu-id="aa8a3-116">A magánjellegű konfiguráció titkosításához használt tanúsítvány-ujjlenyomatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="aa8a3-117">Ez a tanúsítvány már létezik a tanúsítványtárolóban.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="aa8a3-118">Ha nem ad meg tanúsítványt, a parancsmag létrehoz egy tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa8a3-119">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="aa8a3-119">-Credential</span></span>
<span data-ttu-id="aa8a3-120">Adja meg a távoli asztalhoz engedélyezni kívánt hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-120">Specifies the credentials to enable for remote desktop.</span></span>
<span data-ttu-id="aa8a3-121">A hitelesítő adatok tartalmazzák a felhasználónevet és a jelszót.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-121">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa8a3-122">-Lejárat</span><span class="sxs-lookup"><span data-stu-id="aa8a3-122">-Expiration</span></span>
<span data-ttu-id="aa8a3-123">Megadja azt a dátum-idő objektumot, amely lehetővé teszi, hogy a felhasználó megadhatja, hogy mikor jár le a felhasználói fiók.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-123">Specifies a date time object that allows the user to specify when the user account expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa8a3-124">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="aa8a3-124">-ExtensionId</span></span>
<span data-ttu-id="aa8a3-125">A bővítmény AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-125">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa8a3-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="aa8a3-126">-InformationAction</span></span>
<span data-ttu-id="aa8a3-127">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="aa8a3-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="aa8a3-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aa8a3-129">Folytassa</span><span class="sxs-lookup"><span data-stu-id="aa8a3-129">Continue</span></span>
- <span data-ttu-id="aa8a3-130">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="aa8a3-130">Ignore</span></span>
- <span data-ttu-id="aa8a3-131">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="aa8a3-131">Inquire</span></span>
- <span data-ttu-id="aa8a3-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="aa8a3-132">SilentlyContinue</span></span>
- <span data-ttu-id="aa8a3-133">állj</span><span class="sxs-lookup"><span data-stu-id="aa8a3-133">Stop</span></span>
- <span data-ttu-id="aa8a3-134">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="aa8a3-134">Suspend</span></span>

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

### <span data-ttu-id="aa8a3-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="aa8a3-135">-InformationVariable</span></span>
<span data-ttu-id="aa8a3-136">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="aa8a3-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="aa8a3-137">-Profile</span></span>
<span data-ttu-id="aa8a3-138">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aa8a3-139">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aa8a3-140">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="aa8a3-140">-Role</span></span>
<span data-ttu-id="aa8a3-141">Azt a választható szerepköröket adja meg, amelyekhez a távoli asztali konfigurációt meg szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-141">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="aa8a3-142">Ha ez a paraméter nincs megadva, a program az összes szerepkör alapértelmezett konfigurációjának megfelelően alkalmazza a távoli asztali konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-142">If this parameter is not specified, the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="aa8a3-143">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="aa8a3-143">-ServiceName</span></span>
<span data-ttu-id="aa8a3-144">A központi üzembe helyezés Azure-szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-144">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="aa8a3-145">-Slot</span><span class="sxs-lookup"><span data-stu-id="aa8a3-145">-Slot</span></span>
<span data-ttu-id="aa8a3-146">A módosítani kívánt központi verzió környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-146">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="aa8a3-147">A paraméter elfogadható értékei a következők: termelés, megállóhelyek.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-147">The acceptable values for this parameter are: Production, Staging.</span></span>

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

### <span data-ttu-id="aa8a3-148">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="aa8a3-148">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="aa8a3-149">Egy ujjlenyomat-ujjlenyomat-algoritmust ad meg, amely a tanúsítvány meghatározásához használt ujjlenyomatmal van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-149">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="aa8a3-150">Ez a paraméter nem kötelező, és az alapértelmezett érték az SHA1.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-150">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="aa8a3-151">-Verzió</span><span class="sxs-lookup"><span data-stu-id="aa8a3-151">-Version</span></span>
<span data-ttu-id="aa8a3-152">A bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-152">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa8a3-153">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="aa8a3-153">-X509Certificate</span></span>
<span data-ttu-id="aa8a3-154">Itt adhatja meg azt a x509-tanúsítványt, amelyet a rendszer automatikusan feltölt a felhőalapú szolgáltatásba, és a kiterjesztés privát konfigurációjának titkosítására szolgál.</span><span class="sxs-lookup"><span data-stu-id="aa8a3-154">Specifies an x509 certificate that is automatically uploaded to the cloud service and used for encrypting the private configuration of the extension.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: SetExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa8a3-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa8a3-155">CommonParameters</span></span>
<span data-ttu-id="aa8a3-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa8a3-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa8a3-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa8a3-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa8a3-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa8a3-158">INPUTS</span></span>

## <span data-ttu-id="aa8a3-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa8a3-159">OUTPUTS</span></span>

## <span data-ttu-id="aa8a3-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa8a3-160">NOTES</span></span>

## <span data-ttu-id="aa8a3-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa8a3-161">RELATED LINKS</span></span>

[<span data-ttu-id="aa8a3-162">Get-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="aa8a3-162">Get-AzureServiceRemoteDesktopExtension</span></span>](./Get-AzureServiceRemoteDesktopExtension.md)


