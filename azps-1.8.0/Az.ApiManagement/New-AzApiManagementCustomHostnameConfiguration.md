---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: c7be6a09a6fac8338756609abbd291e22fd9565c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671673"
---
# <span data-ttu-id="709ee-101">New-AzApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="709ee-101">New-AzApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="709ee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="709ee-102">SYNOPSIS</span></span>
<span data-ttu-id="709ee-103">Létrehozza a példányát `PsApiManagementCustomHostNameConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="709ee-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

## <span data-ttu-id="709ee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="709ee-104">SYNTAX</span></span>

### <span data-ttu-id="709ee-105">NoChangeCertificate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="709ee-105">NoChangeCertificate (Default)</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="709ee-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="709ee-106">SslCertificateFromFile</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -PfxPath <String> [-PfxPassword <SecureString>] [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="709ee-107">SslCertificateFromKeyVault</span><span class="sxs-lookup"><span data-stu-id="709ee-107">SslCertificateFromKeyVault</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -KeyVaultId <String> [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="709ee-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="709ee-108">DESCRIPTION</span></span>
<span data-ttu-id="709ee-109">A **New-AzApiManagementCustomHostnameConfiguration** parancsmag egy olyan segítő parancs, amely a **PsApiManagementCustomHostNameConfiguration** példányát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="709ee-109">The **New-AzApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="709ee-110">Ezt a parancsot a New-AzApiManagement és a Set-AzApiManagement parancsmag használja.</span><span class="sxs-lookup"><span data-stu-id="709ee-110">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="709ee-111">Példák</span><span class="sxs-lookup"><span data-stu-id="709ee-111">EXAMPLES</span></span>

### <span data-ttu-id="709ee-112">Példa 1: PsApiManagementCustomHostNameConfiguration-példány létrehozása és inicializálása SSL-tanúsítvánnyal fájlból</span><span class="sxs-lookup"><span data-stu-id="709ee-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="709ee-113">Ezzel a paranccsal létrehozhatja és inicializálhatja a **PsApiManagementCustomHostNameConfiguration** a portálra.</span><span class="sxs-lookup"><span data-stu-id="709ee-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="709ee-114">Ezután létrehoz egy új ApiManagement szolgáltatást az egyéni gépnév-konfigurációval.</span><span class="sxs-lookup"><span data-stu-id="709ee-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="709ee-115">2. példa: a PsApiManagementCustomHostNameConfiguration-példányok létrehozása és inicializálása titkos kulccsal</span><span class="sxs-lookup"><span data-stu-id="709ee-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -AssignIdentity
```

<span data-ttu-id="709ee-116">Ezzel a paranccsal létrehozhatja és inicializálhatja a **PsApiManagementCustomHostNameConfiguration** példányát.</span><span class="sxs-lookup"><span data-stu-id="709ee-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="709ee-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="709ee-117">PARAMETERS</span></span>

### <span data-ttu-id="709ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="709ee-118">-DefaultProfile</span></span>
<span data-ttu-id="709ee-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="709ee-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="709ee-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="709ee-120">-DefaultSslBinding</span></span>
<span data-ttu-id="709ee-121">Azt határozza meg, hogy az érték titkos-e, és hogy titkosított-e.</span><span class="sxs-lookup"><span data-stu-id="709ee-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="709ee-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="709ee-122">This parameter is optional.</span></span>
<span data-ttu-id="709ee-123">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="709ee-123">Default Value is false.</span></span>

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

### <span data-ttu-id="709ee-124">-Hostname (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="709ee-124">-Hostname</span></span>
<span data-ttu-id="709ee-125">Egyéni állomásnév</span><span class="sxs-lookup"><span data-stu-id="709ee-125">Custom Hostname</span></span>

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

### <span data-ttu-id="709ee-126">-HostNameCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="709ee-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="709ee-127">Létező tanúsítvány-konfiguráció</span><span class="sxs-lookup"><span data-stu-id="709ee-127">Existing Certificate Configuration.</span></span>

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

### <span data-ttu-id="709ee-128">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="709ee-128">-HostnameType</span></span>
<span data-ttu-id="709ee-129">Állomásnév típusa</span><span class="sxs-lookup"><span data-stu-id="709ee-129">Hostname Type</span></span>

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

### <span data-ttu-id="709ee-130">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="709ee-130">-KeyVaultId</span></span>
<span data-ttu-id="709ee-131">KeyVaultId az egyéni SSL-tanúsítványt tároló titokra.</span><span class="sxs-lookup"><span data-stu-id="709ee-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

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

### <span data-ttu-id="709ee-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="709ee-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="709ee-133">Azt határozza meg, hogy az érték titkos-e, és hogy titkosított-e.</span><span class="sxs-lookup"><span data-stu-id="709ee-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="709ee-134">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="709ee-134">This parameter is optional.</span></span>
<span data-ttu-id="709ee-135">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="709ee-135">Default Value is false.</span></span>

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

### <span data-ttu-id="709ee-136">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="709ee-136">-PfxPassword</span></span>
<span data-ttu-id="709ee-137">A. pfx tanúsítványfájl jelszava.</span><span class="sxs-lookup"><span data-stu-id="709ee-137">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="709ee-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="709ee-138">-PfxPath</span></span>
<span data-ttu-id="709ee-139">A. pfx tanúsítványfájl elérési útvonala.</span><span class="sxs-lookup"><span data-stu-id="709ee-139">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="709ee-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="709ee-140">CommonParameters</span></span>
<span data-ttu-id="709ee-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="709ee-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="709ee-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="709ee-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="709ee-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="709ee-143">INPUTS</span></span>

### <span data-ttu-id="709ee-144">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="709ee-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="709ee-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="709ee-145">OUTPUTS</span></span>

### <span data-ttu-id="709ee-146">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementCustomHostNameConfiguration</span><span class="sxs-lookup"><span data-stu-id="709ee-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="709ee-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="709ee-147">NOTES</span></span>

## <span data-ttu-id="709ee-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="709ee-148">RELATED LINKS</span></span>

[<span data-ttu-id="709ee-149">Új – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="709ee-149">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="709ee-150">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="709ee-150">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)