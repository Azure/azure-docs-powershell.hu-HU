---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: 2f929fc2968935284024e1112e62b395aa0d545e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679225"
---
# <span data-ttu-id="17bb6-101">New-AzureRmApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="17bb6-101">New-AzureRmApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="17bb6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="17bb6-102">SYNOPSIS</span></span>
<span data-ttu-id="17bb6-103">Létrehozza a példányát `PsApiManagementCustomHostNameConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="17bb6-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17bb6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="17bb6-104">SYNTAX</span></span>

### <span data-ttu-id="17bb6-105">NoChangeCertificate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="17bb6-105">NoChangeCertificate (Default)</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17bb6-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="17bb6-106">SslCertificateFromFile</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultSslBinding] [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17bb6-107">SslCertificateFromKeyVault</span><span class="sxs-lookup"><span data-stu-id="17bb6-107">SslCertificateFromKeyVault</span></span>
```
New-AzureRmApiManagementCustomHostnameConfiguration -Hostname <String>
 -HostnameType <PsApiManagementHostnameType> -KeyVaultId <String> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17bb6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="17bb6-108">DESCRIPTION</span></span>
<span data-ttu-id="17bb6-109">A **New-AzureRmApiManagementCustomHostnameConfiguration** parancsmag egy olyan segítő parancs, amely a **PsApiManagementCustomHostNameConfiguration** példányát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="17bb6-109">The **New-AzureRmApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="17bb6-110">Ezt a parancsot a New-AzureRmApiManagement és a Set-AzureRmApiManagement parancsmag használja.</span><span class="sxs-lookup"><span data-stu-id="17bb6-110">This command is used with the New-AzureRmApiManagement and Set-AzureRmApiManagement cmdlet.</span></span>

## <span data-ttu-id="17bb6-111">Példák</span><span class="sxs-lookup"><span data-stu-id="17bb6-111">EXAMPLES</span></span>

### <span data-ttu-id="17bb6-112">Példa 1: PsApiManagementCustomHostNameConfiguration-példány létrehozása és inicializálása SSL-tanúsítvánnyal fájlból</span><span class="sxs-lookup"><span data-stu-id="17bb6-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="17bb6-113">Ezzel a paranccsal létrehozhatja és inicializálhatja a **PsApiManagementCustomHostNameConfiguration** a portálra.</span><span class="sxs-lookup"><span data-stu-id="17bb6-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="17bb6-114">Ezután létrehoz egy új ApiManagement szolgáltatást az egyéni gépnév-konfigurációval.</span><span class="sxs-lookup"><span data-stu-id="17bb6-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="17bb6-115">2. példa: a PsApiManagementCustomHostNameConfiguration-példányok létrehozása és inicializálása titkos kulccsal</span><span class="sxs-lookup"><span data-stu-id="17bb6-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -AssignIdentity
```

<span data-ttu-id="17bb6-116">Ezzel a paranccsal létrehozhatja és inicializálhatja a **PsApiManagementCustomHostNameConfiguration** példányát.</span><span class="sxs-lookup"><span data-stu-id="17bb6-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="17bb6-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="17bb6-117">PARAMETERS</span></span>

### <span data-ttu-id="17bb6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17bb6-118">-DefaultProfile</span></span>
<span data-ttu-id="17bb6-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17bb6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17bb6-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="17bb6-120">-DefaultSslBinding</span></span>
<span data-ttu-id="17bb6-121">Azt határozza meg, hogy az érték titkos-e, és hogy titkosított-e.</span><span class="sxs-lookup"><span data-stu-id="17bb6-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="17bb6-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="17bb6-122">This parameter is optional.</span></span>
<span data-ttu-id="17bb6-123">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="17bb6-123">Default Value is false.</span></span>

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

### <span data-ttu-id="17bb6-124">-Hostname (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="17bb6-124">-Hostname</span></span>
<span data-ttu-id="17bb6-125">Egyéni állomásnév</span><span class="sxs-lookup"><span data-stu-id="17bb6-125">Custom Hostname</span></span>

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

### <span data-ttu-id="17bb6-126">-HostNameCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="17bb6-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="17bb6-127">Létező tanúsítvány-konfiguráció</span><span class="sxs-lookup"><span data-stu-id="17bb6-127">Existing Certificate Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation
Parameter Sets: NoChangeCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17bb6-128">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="17bb6-128">-HostnameType</span></span>
<span data-ttu-id="17bb6-129">Állomásnév típusa</span><span class="sxs-lookup"><span data-stu-id="17bb6-129">Hostname Type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases:
Accepted values: Proxy, Portal, Management, Scm

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17bb6-130">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="17bb6-130">-KeyVaultId</span></span>
<span data-ttu-id="17bb6-131">KeyVaultId az egyéni SSL-tanúsítványt tároló titokra.</span><span class="sxs-lookup"><span data-stu-id="17bb6-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17bb6-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="17bb6-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="17bb6-133">Azt határozza meg, hogy az érték titkos-e, és hogy titkosított-e.</span><span class="sxs-lookup"><span data-stu-id="17bb6-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="17bb6-134">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="17bb6-134">This parameter is optional.</span></span>
<span data-ttu-id="17bb6-135">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="17bb6-135">Default Value is false.</span></span>

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

### <span data-ttu-id="17bb6-136">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="17bb6-136">-PfxPassword</span></span>
<span data-ttu-id="17bb6-137">A. pfx tanúsítványfájl jelszava.</span><span class="sxs-lookup"><span data-stu-id="17bb6-137">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SslCertificateFromFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17bb6-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="17bb6-138">-PfxPath</span></span>
<span data-ttu-id="17bb6-139">A. pfx tanúsítványfájl elérési útvonala.</span><span class="sxs-lookup"><span data-stu-id="17bb6-139">Path to a .pfx certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17bb6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17bb6-140">CommonParameters</span></span>
<span data-ttu-id="17bb6-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="17bb6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17bb6-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17bb6-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17bb6-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="17bb6-143">INPUTS</span></span>

### <span data-ttu-id="17bb6-144">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="17bb6-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="17bb6-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17bb6-145">OUTPUTS</span></span>

### <span data-ttu-id="17bb6-146">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementCustomHostNameConfiguration</span><span class="sxs-lookup"><span data-stu-id="17bb6-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="17bb6-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="17bb6-147">NOTES</span></span>

## <span data-ttu-id="17bb6-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17bb6-148">RELATED LINKS</span></span>

[<span data-ttu-id="17bb6-149">Új – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="17bb6-149">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="17bb6-150">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="17bb6-150">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)
