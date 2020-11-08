---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2E738CEF-BBDD-425D-B12C-86FF7C45A634
online version: ''
schema: 2.0.0
ms.openlocfilehash: 518528d4af8889cf36b30c417e0170e0ea228ebf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016047"
---
# <span data-ttu-id="4f3ec-101">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="4f3ec-101">Set-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="4f3ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4f3ec-102">SYNOPSIS</span></span>
<span data-ttu-id="4f3ec-103">Engedélyezi az Azure Diagnostics bővítményt a megadott szerepkörökön vagy az összes szerepkörön egy telepített szolgáltatásban vagy a központi telepítésben.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-103">Enables Azure Diagnostics extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="4f3ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4f3ec-104">SYNTAX</span></span>

### <span data-ttu-id="4f3ec-105">SetExtension (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4f3ec-105">SetExtension (Default)</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-Version] <String>] [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f3ec-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="4f3ec-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-CertificateThumbprint] <String>] [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-Version] <String>] [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f3ec-107">SetExtensionUsingDiagnosticsConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f3ec-107">SetExtensionUsingDiagnosticsConfiguration</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-DiagnosticsConfiguration] <ExtensionConfigurationInput[]> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4f3ec-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4f3ec-108">DESCRIPTION</span></span>
<span data-ttu-id="4f3ec-109">A **set-AzureServiceDiagnosticsExtension** parancsmag lehetővé teszi az Azure Diagnostics bővítményt a megadott szerepkörökben vagy a központi telepítésben szereplő összes szerepkörön.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-109">The **Set-AzureServiceDiagnosticsExtension** cmdlet enables Azure Diagnostics extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="4f3ec-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4f3ec-110">EXAMPLES</span></span>

### <span data-ttu-id="4f3ec-111">1. példa: az Azure Diagnostics bővítmény engedélyezése</span><span class="sxs-lookup"><span data-stu-id="4f3ec-111">Example 1: Enable Azure Diagnostics extension</span></span>
```
PS C:\> Set-AzureServiceDiagnosticsExtension -ServiceName $Svc -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML
```

<span data-ttu-id="4f3ec-112">Ez a parancs engedélyezi az Azure Diagnostics bővítményt az összes szerepkörhöz.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-112">This command enables the Azure Diagnostics extension for all roles.</span></span>

### <span data-ttu-id="4f3ec-113">2. példa: az Azure Diagnostics bővítmény engedélyezése meghatározott szerepkörhöz</span><span class="sxs-lookup"><span data-stu-id="4f3ec-113">Example 2: Enable Azure Diagnostics extension for a specified role</span></span>
```
PS C:\> Set-AzureServiceDiagnosticsExtension -ServiceName $Svc -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML -Role "WebRole01"
```

<span data-ttu-id="4f3ec-114">Ez a parancs engedélyezi az Azure Diagnostics bővítményt egy adott szerepkörhöz.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-114">This command enables the Azure Diagnostics extension for a specified role.</span></span>

## <span data-ttu-id="4f3ec-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4f3ec-115">PARAMETERS</span></span>

### <span data-ttu-id="4f3ec-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="4f3ec-116">-CertificateThumbprint</span></span>
<span data-ttu-id="4f3ec-117">A magánjellegű konfiguráció titkosításához használt tanúsítvány-ujjlenyomatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="4f3ec-118">Ez a tanúsítvány már létezik a tanúsítványtárolóban.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="4f3ec-119">Ha nem ad meg tanúsítványt, a parancsmag létrehoz egy tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3ec-120">-DiagnosticsConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f3ec-120">-DiagnosticsConfiguration</span></span>
<span data-ttu-id="4f3ec-121">Az Azure Diagnostics konfigurációjának tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-121">Specifies an array of configuration for Azure Diagnostics.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: SetExtensionUsingDiagnosticsConfiguration
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3ec-122">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="4f3ec-122">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="4f3ec-123">Az Azure Diagnostics konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-123">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="4f3ec-124">A séma letöltéséhez a következő parancsot használja:</span><span class="sxs-lookup"><span data-stu-id="4f3ec-124">You can download the schema by using the following command:</span></span> 

`(Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'`

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3ec-125">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="4f3ec-125">-ExtensionId</span></span>
<span data-ttu-id="4f3ec-126">A bővítmény AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-126">Specifies the extension ID</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3ec-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4f3ec-127">-InformationAction</span></span>
<span data-ttu-id="4f3ec-128">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4f3ec-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4f3ec-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4f3ec-130">Folytassa</span><span class="sxs-lookup"><span data-stu-id="4f3ec-130">Continue</span></span>
- <span data-ttu-id="4f3ec-131">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="4f3ec-131">Ignore</span></span>
- <span data-ttu-id="4f3ec-132">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="4f3ec-132">Inquire</span></span>
- <span data-ttu-id="4f3ec-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4f3ec-133">SilentlyContinue</span></span>
- <span data-ttu-id="4f3ec-134">állj</span><span class="sxs-lookup"><span data-stu-id="4f3ec-134">Stop</span></span>
- <span data-ttu-id="4f3ec-135">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="4f3ec-135">Suspend</span></span>

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

### <span data-ttu-id="4f3ec-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4f3ec-136">-InformationVariable</span></span>
<span data-ttu-id="4f3ec-137">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4f3ec-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="4f3ec-138">-Profile</span></span>
<span data-ttu-id="4f3ec-139">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4f3ec-140">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4f3ec-141">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="4f3ec-141">-Role</span></span>
<span data-ttu-id="4f3ec-142">Itt adhatja meg az Azure Diagnostics konfigurációjának megadására szolgáló szerepkörök tetszőleges sorát.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-142">Specifies an optional array of roles for which to specify the Azure Diagnostics configuration.</span></span>
<span data-ttu-id="4f3ec-143">Ha nem adja meg ezt a paramétert, a diagnosztika konfigurációja az összes szerepkör alapértelmezett konfigurációjának megfelelően jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-143">If you do not specify this parameter, the diagnostics configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3ec-144">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="4f3ec-144">-ServiceName</span></span>
<span data-ttu-id="4f3ec-145">A központi üzembe helyezés Azure-szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-145">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="4f3ec-146">-Slot</span><span class="sxs-lookup"><span data-stu-id="4f3ec-146">-Slot</span></span>
<span data-ttu-id="4f3ec-147">A módosítani kívánt központi verzió környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-147">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="4f3ec-148">A paraméter elfogadható értékei a következők: termelés vagy megállóhely.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-148">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="4f3ec-149">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f3ec-149">-StorageAccountEndpoint</span></span>
<span data-ttu-id="4f3ec-150">A tárolási fiók végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-150">Specifies a storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3ec-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4f3ec-151">-StorageAccountKey</span></span>
<span data-ttu-id="4f3ec-152">A tárolási fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-152">Specifies a storage account key.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3ec-153">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4f3ec-153">-StorageAccountName</span></span>
<span data-ttu-id="4f3ec-154">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-154">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3ec-155">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="4f3ec-155">-StorageContext</span></span>
<span data-ttu-id="4f3ec-156">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-156">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3ec-157">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="4f3ec-157">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="4f3ec-158">A tanúsítvány meghatározására szolgáló ujjlenyomat-algoritmust ad meg.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-158">Specifies a thumbprint hashing algorithm that is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="4f3ec-159">Ez a paraméter nem kötelező, és az alapértelmezett érték az SHA1.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-159">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3ec-160">-Verzió</span><span class="sxs-lookup"><span data-stu-id="4f3ec-160">-Version</span></span>
<span data-ttu-id="4f3ec-161">A bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-161">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3ec-162">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="4f3ec-162">-X509Certificate</span></span>
<span data-ttu-id="4f3ec-163">Egy X. 509 formátumú tanúsítványt ad meg, amely a megadott módon automatikusan a felhőalapú szolgáltatásba töltődik be, és a privát konfiguráció titkosítására szolgál.</span><span class="sxs-lookup"><span data-stu-id="4f3ec-163">Specifies an X.509 certificate that, when specified, is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="4f3ec-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f3ec-164">CommonParameters</span></span>
<span data-ttu-id="4f3ec-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4f3ec-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f3ec-166">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f3ec-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f3ec-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f3ec-167">INPUTS</span></span>

## <span data-ttu-id="4f3ec-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f3ec-168">OUTPUTS</span></span>

## <span data-ttu-id="4f3ec-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4f3ec-169">NOTES</span></span>

## <span data-ttu-id="4f3ec-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f3ec-170">RELATED LINKS</span></span>

[<span data-ttu-id="4f3ec-171">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="4f3ec-171">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="4f3ec-172">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="4f3ec-172">Remove-AzureServiceDiagnosticsExtension</span></span>](./Remove-AzureServiceDiagnosticsExtension.md)


