---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1F76C63E-5289-4F88-9522-3FF4EF732908
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a232ec03da38ea3d527dcd9aa214dbf681bcc6a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015898"
---
# <span data-ttu-id="2f4a1-101">New-AzureServiceDiagnosticsExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="2f4a1-101">New-AzureServiceDiagnosticsExtensionConfig</span></span>

## <span data-ttu-id="2f4a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f4a1-102">SYNOPSIS</span></span>
<span data-ttu-id="2f4a1-103">Diagnosztikai bővítmény konfigurációjának létrehozása meghatározott szerepkör (ek) vagy minden szerepkör esetében.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-103">Generates a configuration for a diagnostics extension for specified role(s) or all roles.</span></span>

## <span data-ttu-id="2f4a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f4a1-104">SYNTAX</span></span>

### <span data-ttu-id="2f4a1-105">NewExtension (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f4a1-105">NewExtension (Default)</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2f4a1-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="2f4a1-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>]
 [[-StorageContext] <AzureStorageContext>] [-DiagnosticsConfigurationPath] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f4a1-107">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="2f4a1-107">SetExtensionUsingThumbprint</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2f4a1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f4a1-108">DESCRIPTION</span></span>
<span data-ttu-id="2f4a1-109">A **New-AzureServiceDiagnosticsExtensionConfig** parancsmag a megadott szerepkörök vagy az összes szerepkör diagnosztikai bővítményének konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-109">The **New-AzureServiceDiagnosticsExtensionConfig** cmdlet generates a configuration for a diagnostics extension for specified roles or all roles.</span></span>

## <span data-ttu-id="2f4a1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2f4a1-110">EXAMPLES</span></span>

### <span data-ttu-id="2f4a1-111">Példa 1: az Azure Diagnostics bővítmény létrehozása a felhőalapú szolgáltatás összes szerepköréhez</span><span class="sxs-lookup"><span data-stu-id="2f4a1-111">Example 1: Create the Azure Diagnostics extension for all roles in the cloud service</span></span>
```
PS C:\> $WadConfig = New-AzureServiceDiagnosticExtensionConfig -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML
```

<span data-ttu-id="2f4a1-112">Ez a parancs létrehozza az Azure Diagnostics bővítményt a felhőalapú szolgáltatás összes szerepköréhez.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-112">This command creates the Azure Diagnostics extension for all of the roles in the cloud service.</span></span>

### <span data-ttu-id="2f4a1-113">2. példa: az Azure Diagnostics bővítmény létrehozása szerepkörhöz</span><span class="sxs-lookup"><span data-stu-id="2f4a1-113">Example 2: Create the Azure Diagnostics extension for a role</span></span>
```
PS C:\> $WadConfig = New-AzureServiceDiagnosticExtensionConfig -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML -Role "WebRole1"
```

<span data-ttu-id="2f4a1-114">Ez a parancs létrehozza az Azure Diagnostics bővítményt a felhőalapú szolgáltatás szerepkör-WebRole01.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-114">This command creates the Azure Diagnostics extension for the role WebRole01 in the cloud service.</span></span>

## <span data-ttu-id="2f4a1-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f4a1-115">PARAMETERS</span></span>

### <span data-ttu-id="2f4a1-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="2f4a1-116">-CertificateThumbprint</span></span>
<span data-ttu-id="2f4a1-117">A magánjellegű konfiguráció titkosításához használt tanúsítvány-ujjlenyomatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="2f4a1-118">Ez a tanúsítvány már létezik a tanúsítványtárolóban.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="2f4a1-119">Ha nem ad meg tanúsítványt, a parancsmag létrehoz egy tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="2f4a1-120">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="2f4a1-120">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="2f4a1-121">A diagnosztikai konfiguráció elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-121">Specifies the diagnostics configuration path.</span></span>

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

### <span data-ttu-id="2f4a1-122">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="2f4a1-122">-ExtensionId</span></span>
<span data-ttu-id="2f4a1-123">A bővítmény AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-123">Specifies the extension ID.</span></span>

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

### <span data-ttu-id="2f4a1-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2f4a1-124">-InformationAction</span></span>
<span data-ttu-id="2f4a1-125">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2f4a1-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2f4a1-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2f4a1-127">Folytassa</span><span class="sxs-lookup"><span data-stu-id="2f4a1-127">Continue</span></span>
- <span data-ttu-id="2f4a1-128">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="2f4a1-128">Ignore</span></span>
- <span data-ttu-id="2f4a1-129">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="2f4a1-129">Inquire</span></span>
- <span data-ttu-id="2f4a1-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2f4a1-130">SilentlyContinue</span></span>
- <span data-ttu-id="2f4a1-131">állj</span><span class="sxs-lookup"><span data-stu-id="2f4a1-131">Stop</span></span>
- <span data-ttu-id="2f4a1-132">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="2f4a1-132">Suspend</span></span>

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

### <span data-ttu-id="2f4a1-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2f4a1-133">-InformationVariable</span></span>
<span data-ttu-id="2f4a1-134">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2f4a1-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="2f4a1-135">-Profile</span></span>
<span data-ttu-id="2f4a1-136">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-136">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2f4a1-137">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2f4a1-138">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="2f4a1-138">-Role</span></span>
<span data-ttu-id="2f4a1-139">A szerepkörök választható tömböket adja meg a diagnosztikai konfiguráció megadásához.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-139">Specifies an optional array of roles to specify the diagnostics configuration for.</span></span>
<span data-ttu-id="2f4a1-140">Ha nem adja meg, akkor az összes szerepkör alapértelmezett konfigurációjaként alkalmazza a diagnosztikai konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-140">If not specified the diagnostics configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4a1-141">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f4a1-141">-StorageAccountEndpoint</span></span>
<span data-ttu-id="2f4a1-142">A tárolási fiók végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-142">Specifies the storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4a1-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2f4a1-143">-StorageAccountKey</span></span>
<span data-ttu-id="2f4a1-144">A tárolási fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-144">Specifies the storage account key.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4a1-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2f4a1-145">-StorageAccountName</span></span>
<span data-ttu-id="2f4a1-146">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-146">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4a1-147">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="2f4a1-147">-StorageContext</span></span>
<span data-ttu-id="2f4a1-148">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-148">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4a1-149">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="2f4a1-149">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="2f4a1-150">Egy ujjlenyomat-ujjlenyomat-algoritmust ad meg, amely a tanúsítvány meghatározásához használt ujjlenyomatmal van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-150">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="2f4a1-151">Ez a paraméter nem kötelező, és az alapértelmezett érték az SHA1.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-151">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="2f4a1-152">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="2f4a1-152">-X509Certificate</span></span>
<span data-ttu-id="2f4a1-153">Itt adhatja meg azt az X. 509 tanúsítványt, amelyet a rendszer automatikusan feltölt a felhőalapú szolgáltatásba, és a privát konfiguráció titkosítására szolgál.</span><span class="sxs-lookup"><span data-stu-id="2f4a1-153">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="2f4a1-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f4a1-154">CommonParameters</span></span>
<span data-ttu-id="2f4a1-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f4a1-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f4a1-156">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f4a1-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f4a1-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f4a1-157">INPUTS</span></span>

## <span data-ttu-id="2f4a1-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f4a1-158">OUTPUTS</span></span>

## <span data-ttu-id="2f4a1-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f4a1-159">NOTES</span></span>

## <span data-ttu-id="2f4a1-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f4a1-160">RELATED LINKS</span></span>

[<span data-ttu-id="2f4a1-161">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="2f4a1-161">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="2f4a1-162">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="2f4a1-162">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


