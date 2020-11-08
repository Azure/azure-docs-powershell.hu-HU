---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D37920D3-AF6C-4CFC-B9A3-8ED931AEC0DC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 318683c26d05c624549363ff1afe4a2b963c1fe6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015447"
---
# <span data-ttu-id="01183-101">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="01183-101">Set-AzureServiceExtension</span></span>

## <span data-ttu-id="01183-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01183-102">SYNOPSIS</span></span>
<span data-ttu-id="01183-103">Felhőbeli szolgáltatás bővítményt ad hozzá a bevezetéshez.</span><span class="sxs-lookup"><span data-stu-id="01183-103">Adds a cloud service extension to a deployment.</span></span>

## <span data-ttu-id="01183-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01183-104">SYNTAX</span></span>

### <span data-ttu-id="01183-105">SetExtension (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="01183-105">SetExtension (Default)</span></span>
```
Set-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-PublicConfiguration] <String> [-PrivateConfiguration] <String>
 [-Version] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="01183-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="01183-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-PublicConfiguration] <String> [-PrivateConfiguration] <String>
 [-Version] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="01183-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="01183-107">DESCRIPTION</span></span>
<span data-ttu-id="01183-108">A **set-AzureServiceExtension** parancsmag a Felhőbeli szolgáltatások bővítményét hozzáadja a központi üzembe helyezéshez.</span><span class="sxs-lookup"><span data-stu-id="01183-108">The **Set-AzureServiceExtension** cmdlet adds a cloud service extension to a deployment.</span></span>

## <span data-ttu-id="01183-109">Példák</span><span class="sxs-lookup"><span data-stu-id="01183-109">EXAMPLES</span></span>

### <span data-ttu-id="01183-110">1. példa: Felhőbeli szolgáltatás hozzáadása a központi üzembe helyezéshez</span><span class="sxs-lookup"><span data-stu-id="01183-110">Example 1: Add a cloud service to a deployment</span></span>
```
PS C:\> Set-AzureServiceExtension -Service $Svc -Slot "Production" -ExtensionName "RDP" -Version "1.0" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -PublicConfiguration $P1 -PrivateConfiguration $P2;
```

<span data-ttu-id="01183-111">Ez a parancs Felhőbeli szolgáltatást ad a bevezetéshez.</span><span class="sxs-lookup"><span data-stu-id="01183-111">This command adds a cloud service to a deployment.</span></span>

### <span data-ttu-id="01183-112">2. példa: Felhőbeli szolgáltatás hozzáadása adott szerepkör telepítéséhez</span><span class="sxs-lookup"><span data-stu-id="01183-112">Example 2: Add a cloud service to a deployment for a specified role</span></span>
```
PS C:\> Set-AzureServiceExtension -Service $Svc -Slot "Production" -Role "WebRole1" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -PublicConfiguration $P1 -PrivateConfiguration $P2;
```

<span data-ttu-id="01183-113">Ez a parancs Felhőbeli szolgáltatást ad a központi üzembe helyezéshez meghatározott szerepkörhöz.</span><span class="sxs-lookup"><span data-stu-id="01183-113">This command adds a cloud service to a deployment for a specified role.</span></span>

## <span data-ttu-id="01183-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01183-114">PARAMETERS</span></span>

### <span data-ttu-id="01183-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="01183-115">-CertificateThumbprint</span></span>
<span data-ttu-id="01183-116">A magánjellegű konfiguráció titkosításához használt tanúsítvány-ujjlenyomatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="01183-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="01183-117">Ez a tanúsítvány már létezik a tanúsítványtárolóban.</span><span class="sxs-lookup"><span data-stu-id="01183-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="01183-118">Ha nem ad meg tanúsítványt, a parancsmag létrehoz egy tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="01183-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="01183-119">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="01183-119">-ExtensionId</span></span>
<span data-ttu-id="01183-120">A bővítmény AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="01183-120">Specifies the extension ID.</span></span>

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

### <span data-ttu-id="01183-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="01183-121">-ExtensionName</span></span>
<span data-ttu-id="01183-122">A kiterjesztés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="01183-122">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01183-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="01183-123">-InformationAction</span></span>
<span data-ttu-id="01183-124">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="01183-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="01183-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="01183-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="01183-126">Folytassa</span><span class="sxs-lookup"><span data-stu-id="01183-126">Continue</span></span>
- <span data-ttu-id="01183-127">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="01183-127">Ignore</span></span>
- <span data-ttu-id="01183-128">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="01183-128">Inquire</span></span>
- <span data-ttu-id="01183-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="01183-129">SilentlyContinue</span></span>
- <span data-ttu-id="01183-130">állj</span><span class="sxs-lookup"><span data-stu-id="01183-130">Stop</span></span>
- <span data-ttu-id="01183-131">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="01183-131">Suspend</span></span>

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

### <span data-ttu-id="01183-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="01183-132">-InformationVariable</span></span>
<span data-ttu-id="01183-133">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="01183-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="01183-134">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="01183-134">-PrivateConfiguration</span></span>
<span data-ttu-id="01183-135">A privát konfiguráció szövegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="01183-135">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01183-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="01183-136">-Profile</span></span>
<span data-ttu-id="01183-137">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="01183-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="01183-138">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="01183-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="01183-139">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="01183-139">-ProviderNamespace</span></span>
<span data-ttu-id="01183-140">A bővítmény-szolgáltató névterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="01183-140">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01183-141">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="01183-141">-PublicConfiguration</span></span>
<span data-ttu-id="01183-142">A nyilvános konfiguráció szövegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="01183-142">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01183-143">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="01183-143">-Role</span></span>
<span data-ttu-id="01183-144">Azt a választható szerepköröket adja meg, amelyekhez a távoli asztali konfigurációt meg szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="01183-144">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="01183-145">Ha ez a paraméter nincs megadva, a program az összes szerepkör alapértelmezett konfigurációjának megfelelően alkalmazza a távoli asztali konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="01183-145">If this parameter is not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="01183-146">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="01183-146">-ServiceName</span></span>
<span data-ttu-id="01183-147">A központi üzembe helyezés Azure-szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="01183-147">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="01183-148">-Slot</span><span class="sxs-lookup"><span data-stu-id="01183-148">-Slot</span></span>
<span data-ttu-id="01183-149">A módosítani kívánt központi verzió környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="01183-149">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="01183-150">Érvényes értékek: a termelés vagy a megállóhely.</span><span class="sxs-lookup"><span data-stu-id="01183-150">Valid values are: Production or Staging.</span></span>

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

### <span data-ttu-id="01183-151">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="01183-151">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="01183-152">A tanúsítványt azonosító ujjlenyomat-ujjlenyomat-algoritmust adja meg.</span><span class="sxs-lookup"><span data-stu-id="01183-152">Specifies the thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="01183-153">Ez a paraméter nem kötelező, és az alapértelmezett érték az SHA1.</span><span class="sxs-lookup"><span data-stu-id="01183-153">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="01183-154">-Verzió</span><span class="sxs-lookup"><span data-stu-id="01183-154">-Version</span></span>
<span data-ttu-id="01183-155">A bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="01183-155">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01183-156">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="01183-156">-X509Certificate</span></span>
<span data-ttu-id="01183-157">Itt adhatja meg azt az X. 509 tanúsítványt, amelyet a rendszer automatikusan feltölt a felhőalapú szolgáltatásba, és a privát konfiguráció titkosítására szolgál.</span><span class="sxs-lookup"><span data-stu-id="01183-157">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="01183-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01183-158">CommonParameters</span></span>
<span data-ttu-id="01183-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01183-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01183-160">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01183-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01183-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01183-161">INPUTS</span></span>

## <span data-ttu-id="01183-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01183-162">OUTPUTS</span></span>

## <span data-ttu-id="01183-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01183-163">NOTES</span></span>

## <span data-ttu-id="01183-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01183-164">RELATED LINKS</span></span>

[<span data-ttu-id="01183-165">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="01183-165">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="01183-166">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="01183-166">Remove-AzureServiceExtension</span></span>](./Remove-AzureServiceExtension.md)


