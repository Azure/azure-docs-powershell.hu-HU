---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 75525d3c77c3e2113c0e3cff5a7741ab916d7485
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011933"
---
# <span data-ttu-id="43830-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="43830-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="43830-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43830-102">SYNOPSIS</span></span>
<span data-ttu-id="43830-103">Ismerje meg az identitás-szolgáltató konfigurációjának részleteit.</span><span class="sxs-lookup"><span data-stu-id="43830-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="43830-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43830-104">SYNTAX</span></span>

### <span data-ttu-id="43830-105">AllIdentityProviders (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43830-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43830-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="43830-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43830-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="43830-107">DESCRIPTION</span></span>
<span data-ttu-id="43830-108">Ismerje meg az identitás-szolgáltató konfigurációjának részleteit.</span><span class="sxs-lookup"><span data-stu-id="43830-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="43830-109">Példák</span><span class="sxs-lookup"><span data-stu-id="43830-109">EXAMPLES</span></span>

### <span data-ttu-id="43830-110">1. példa: az összes személyazonosság-szolgáltató beszerzése</span><span class="sxs-lookup"><span data-stu-id="43830-110">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="43830-111">A szolgáltatás minden identitás-szolgáltatója konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="43830-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="43830-112">2. példa: a AAD típusú identitás-szolgáltató beszerzése</span><span class="sxs-lookup"><span data-stu-id="43830-112">Example 2: Get the AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $apimContext -Type Aad


Type                     : Aad
ClientId                 : aaa
ClientSecret             : xxxxx
AllowedTenants           : {contosotest.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         :
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             :
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/Aad
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="43830-113">Az Azure Active Directory identitás-szolgáltatójának konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="43830-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="43830-114">3. példa: a AAD B2C típusú személyazonosság-szolgáltató beszerzése</span><span class="sxs-lookup"><span data-stu-id="43830-114">Example 3: Get the AAD B2C Type Identity Provider</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $context -Type AadB2C


Type                     : AadB2C
ClientId                 : f02dafe2-b8b8-48ec-a38e-27e5c16c51e5
ClientSecret             : xxxxxx
AllowedTenants           : {contosoaadb2c.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_policy-signup
SigninPolicyName         : B2C_1_policy-signin
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             : contosoaadb2c.onmicrosoft.com
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="43830-115">Az Azure Active Directory identitás-szolgáltatójának konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="43830-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="43830-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43830-116">PARAMETERS</span></span>

### <span data-ttu-id="43830-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="43830-117">-Context</span></span>
<span data-ttu-id="43830-118">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="43830-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="43830-119">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="43830-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43830-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43830-120">-DefaultProfile</span></span>
<span data-ttu-id="43830-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43830-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43830-122">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="43830-122">-Type</span></span>
<span data-ttu-id="43830-123">Egy identitás-szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="43830-123">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="43830-124">Ha meg van adva, az azonosító segítségével megpróbálja megtalálni az identitás-szolgáltató konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="43830-124">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="43830-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="43830-125">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43830-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43830-126">CommonParameters</span></span>
<span data-ttu-id="43830-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43830-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43830-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="43830-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43830-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43830-129">INPUTS</span></span>

### <span data-ttu-id="43830-130">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="43830-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="43830-131">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="43830-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="43830-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43830-132">OUTPUTS</span></span>

### <span data-ttu-id="43830-133">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="43830-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="43830-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43830-134">NOTES</span></span>

## <span data-ttu-id="43830-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43830-135">RELATED LINKS</span></span>
