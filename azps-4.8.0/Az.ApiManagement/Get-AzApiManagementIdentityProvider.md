---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: b267fc854127c1cb098481ac483a7572c8b2e12f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025606"
---
# <span data-ttu-id="47496-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="47496-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="47496-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47496-102">SYNOPSIS</span></span>
<span data-ttu-id="47496-103">Ismerje meg az identitás-szolgáltató konfigurációjának részleteit.</span><span class="sxs-lookup"><span data-stu-id="47496-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="47496-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47496-104">SYNTAX</span></span>

### <span data-ttu-id="47496-105">AllIdentityProviders (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="47496-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47496-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="47496-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47496-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="47496-107">DESCRIPTION</span></span>
<span data-ttu-id="47496-108">Ismerje meg az identitás-szolgáltató konfigurációjának részleteit.</span><span class="sxs-lookup"><span data-stu-id="47496-108">Get the identity provider configuration details.</span></span>
<span data-ttu-id="47496-109">A ClientSecret nem fog szerepelni az eredmény részletei között.</span><span class="sxs-lookup"><span data-stu-id="47496-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="47496-110">Az ügyfél titkának beszerzéséhez használja a **Get-AzApiManagementIdentityProviderClientSecret**.</span><span class="sxs-lookup"><span data-stu-id="47496-110">To get client secret, use **Get-AzApiManagementIdentityProviderClientSecret**.</span></span>

## <span data-ttu-id="47496-111">Példák</span><span class="sxs-lookup"><span data-stu-id="47496-111">EXAMPLES</span></span>

### <span data-ttu-id="47496-112">1. példa: az összes személyazonosság-szolgáltató beszerzése</span><span class="sxs-lookup"><span data-stu-id="47496-112">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="47496-113">A szolgáltatás minden identitás-szolgáltatója konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="47496-113">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="47496-114">2. példa: a AAD típusú identitás-szolgáltató beszerzése</span><span class="sxs-lookup"><span data-stu-id="47496-114">Example 2: Get the AAD Type Identity Provider</span></span>
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

<span data-ttu-id="47496-115">Az Azure Active Directory identitás-szolgáltatójának konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="47496-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="47496-116">3. példa: a AAD B2C típusú személyazonosság-szolgáltató beszerzése</span><span class="sxs-lookup"><span data-stu-id="47496-116">Example 3: Get the AAD B2C Type Identity Provider</span></span>
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

<span data-ttu-id="47496-117">Az Azure Active Directory identitás-szolgáltatójának konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="47496-117">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="47496-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47496-118">PARAMETERS</span></span>

### <span data-ttu-id="47496-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="47496-119">-Context</span></span>
<span data-ttu-id="47496-120">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="47496-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="47496-121">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="47496-121">This parameter is required.</span></span>

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

### <span data-ttu-id="47496-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47496-122">-DefaultProfile</span></span>
<span data-ttu-id="47496-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47496-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47496-124">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="47496-124">-Type</span></span>
<span data-ttu-id="47496-125">Egy identitás-szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="47496-125">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="47496-126">Ha meg van adva, az azonosító segítségével megpróbálja megtalálni az identitás-szolgáltató konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="47496-126">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="47496-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="47496-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="47496-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47496-128">CommonParameters</span></span>
<span data-ttu-id="47496-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47496-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47496-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="47496-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47496-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47496-131">INPUTS</span></span>

### <span data-ttu-id="47496-132">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="47496-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="47496-133">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="47496-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="47496-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47496-134">OUTPUTS</span></span>

### <span data-ttu-id="47496-135">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="47496-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="47496-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47496-136">NOTES</span></span>

## <span data-ttu-id="47496-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47496-137">RELATED LINKS</span></span>
