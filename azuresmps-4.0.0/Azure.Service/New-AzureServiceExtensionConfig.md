---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E27283AF-4057-48D9-9F08-7D36290DD907
online version: ''
schema: 2.0.0
ms.openlocfilehash: dfe55fb2ced2275eae06e96480249acd99d3ad6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015896"
---
# <span data-ttu-id="3bab6-101">New-AzureServiceExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="3bab6-101">New-AzureServiceExtensionConfig</span></span>

## <span data-ttu-id="3bab6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3bab6-102">SYNOPSIS</span></span>
<span data-ttu-id="3bab6-103">Felhőbeli szolgáltatások bővítményének konfigurációját hozza létre a bevezetéshez.</span><span class="sxs-lookup"><span data-stu-id="3bab6-103">Creates a cloud service extension configuration for a deployment.</span></span>

## <span data-ttu-id="3bab6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3bab6-104">SYNTAX</span></span>

### <span data-ttu-id="3bab6-105">NewExtension (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3bab6-105">NewExtension (Default)</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String> [-ProviderNamespace] <String>
 [-PublicConfiguration] <String> [-PrivateConfiguration] <String> [-Version] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bab6-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="3bab6-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String> [-ProviderNamespace] <String>
 [-PublicConfiguration] <String> [-PrivateConfiguration] <String> [-Version] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bab6-107">UpdateExtensionStatusParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3bab6-107">UpdateExtensionStatusParameterSetName</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [-ExtensionId] <String> [-ExtensionState] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="3bab6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3bab6-108">DESCRIPTION</span></span>
<span data-ttu-id="3bab6-109">A **New-AzureServiceExtensionConfig** parancsmag létrehoz egy felhőalapú szolgáltatás-bővítmény konfigurációját a központi üzembe helyezéshez.</span><span class="sxs-lookup"><span data-stu-id="3bab6-109">The **New-AzureServiceExtensionConfig** cmdlet creates a cloud service extension configuration for a deployment.</span></span>

## <span data-ttu-id="3bab6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3bab6-110">EXAMPLES</span></span>

### <span data-ttu-id="3bab6-111">Példa 1: bővítmény-konfiguráció létrehozása</span><span class="sxs-lookup"><span data-stu-id="3bab6-111">Example 1: Create an extension configuration</span></span>
```
PS C:\> New-AzureServiceExtensionConfig -ExtensionName 'RDP' -Version '1.0' -ProviderNamespace Microsoft.Windows.Azure.Extensions -PublicConfiguration $p1 -PrivateConfiguration $p2;
```

<span data-ttu-id="3bab6-112">Ez a parancs a bővítmények konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bab6-112">This command specifies an extension configuration.</span></span>

### <span data-ttu-id="3bab6-113">2. példa: bővítmény-konfiguráció létrehozása szerepkörhöz</span><span class="sxs-lookup"><span data-stu-id="3bab6-113">Example 2: Create an extension configuration for a role</span></span>
```
PS C:\> New-AzureServiceExtensionConfig -Role WebRole1 -ExtensionName 'RDP' -ProviderNamespace Microsoft.Windows.Azure.Extensions -PublicConfiguration $p1 -PrivateConfiguration $p2;
```

<span data-ttu-id="3bab6-114">Ez a parancs a szerepkör WebRole1 bővítmény-konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bab6-114">This command specifies an extension configuration for the role WebRole1.</span></span>

## <span data-ttu-id="3bab6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3bab6-115">PARAMETERS</span></span>

### <span data-ttu-id="3bab6-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="3bab6-116">-CertificateThumbprint</span></span>
<span data-ttu-id="3bab6-117">A magánjellegű konfiguráció titkosításához használt tanúsítvány-ujjlenyomatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bab6-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="3bab6-118">Ez a tanúsítvány már létezik a tanúsítványtárolóban.</span><span class="sxs-lookup"><span data-stu-id="3bab6-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="3bab6-119">Ha nem ad meg tanúsítványt, a parancsmag létrehoz egy tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="3bab6-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="3bab6-120">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="3bab6-120">-ExtensionId</span></span>
<span data-ttu-id="3bab6-121">A kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bab6-121">Specifies the name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UpdateExtensionStatusParameterSetName
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bab6-122">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="3bab6-122">-ExtensionName</span></span>
<span data-ttu-id="3bab6-123">A kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bab6-123">Specifies the name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bab6-124">-ExtensionState</span><span class="sxs-lookup"><span data-stu-id="3bab6-124">-ExtensionState</span></span>
<span data-ttu-id="3bab6-125">A kiterjesztés állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bab6-125">Specifies the state of the extension.</span></span>
<span data-ttu-id="3bab6-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3bab6-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3bab6-127">Engedélyezése</span><span class="sxs-lookup"><span data-stu-id="3bab6-127">Enable</span></span> 
- <span data-ttu-id="3bab6-128">Megbénít</span><span class="sxs-lookup"><span data-stu-id="3bab6-128">Disable</span></span> 
- <span data-ttu-id="3bab6-129">Eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3bab6-129">Uninstall</span></span>

```yaml
Type: String
Parameter Sets: UpdateExtensionStatusParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bab6-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3bab6-130">-InformationAction</span></span>
<span data-ttu-id="3bab6-131">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="3bab6-131">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3bab6-132">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3bab6-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3bab6-133">Folytassa</span><span class="sxs-lookup"><span data-stu-id="3bab6-133">Continue</span></span>
- <span data-ttu-id="3bab6-134">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="3bab6-134">Ignore</span></span>
- <span data-ttu-id="3bab6-135">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="3bab6-135">Inquire</span></span>
- <span data-ttu-id="3bab6-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3bab6-136">SilentlyContinue</span></span>
- <span data-ttu-id="3bab6-137">állj</span><span class="sxs-lookup"><span data-stu-id="3bab6-137">Stop</span></span>
- <span data-ttu-id="3bab6-138">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="3bab6-138">Suspend</span></span>

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

### <span data-ttu-id="3bab6-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3bab6-139">-InformationVariable</span></span>
<span data-ttu-id="3bab6-140">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="3bab6-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3bab6-141">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="3bab6-141">-PrivateConfiguration</span></span>
<span data-ttu-id="3bab6-142">A privát konfiguráció szövegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bab6-142">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bab6-143">-Profil</span><span class="sxs-lookup"><span data-stu-id="3bab6-143">-Profile</span></span>
<span data-ttu-id="3bab6-144">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3bab6-144">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3bab6-145">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3bab6-145">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3bab6-146">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="3bab6-146">-ProviderNamespace</span></span>
<span data-ttu-id="3bab6-147">A bővítmény szolgáltatójának névteret adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bab6-147">Specifies the Extension's Provider Namespace.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bab6-148">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="3bab6-148">-PublicConfiguration</span></span>
<span data-ttu-id="3bab6-149">A nyilvános konfiguráció szövegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bab6-149">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bab6-150">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="3bab6-150">-Role</span></span>
<span data-ttu-id="3bab6-151">A szerepkörök választható tömbjét adja meg a távoli asztali konfiguráció megadásához.</span><span class="sxs-lookup"><span data-stu-id="3bab6-151">Specifies an optional array of roles to specify the remote desktop configuration for.</span></span>
<span data-ttu-id="3bab6-152">Ha nincs megadva, a program az összes szerepkör alapértelmezett konfigurációjának megfelelően alkalmazza a távoli asztali konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="3bab6-152">If not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="3bab6-153">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="3bab6-153">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="3bab6-154">Egy ujjlenyomat-ujjlenyomat-algoritmust ad meg, amely a tanúsítvány meghatározásához használt ujjlenyomatmal van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="3bab6-154">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="3bab6-155">Ez a paraméter nem kötelező, és az alapértelmezett érték az SHA1.</span><span class="sxs-lookup"><span data-stu-id="3bab6-155">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bab6-156">-Verzió</span><span class="sxs-lookup"><span data-stu-id="3bab6-156">-Version</span></span>
<span data-ttu-id="3bab6-157">A bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bab6-157">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bab6-158">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="3bab6-158">-X509Certificate</span></span>
<span data-ttu-id="3bab6-159">Itt adhatja meg azt a x509-tanúsítványt, amelyet a rendszer automatikusan feltölt a felhőalapú szolgáltatásba, és a privát konfiguráció titkosításához használja.</span><span class="sxs-lookup"><span data-stu-id="3bab6-159">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="3bab6-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bab6-160">CommonParameters</span></span>
<span data-ttu-id="3bab6-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3bab6-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bab6-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bab6-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bab6-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bab6-163">INPUTS</span></span>

## <span data-ttu-id="3bab6-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bab6-164">OUTPUTS</span></span>

## <span data-ttu-id="3bab6-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3bab6-165">NOTES</span></span>

## <span data-ttu-id="3bab6-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3bab6-166">RELATED LINKS</span></span>

[<span data-ttu-id="3bab6-167">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="3bab6-167">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="3bab6-168">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="3bab6-168">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


