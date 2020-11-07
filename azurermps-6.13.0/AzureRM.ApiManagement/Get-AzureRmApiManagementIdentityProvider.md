---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 88147f9f26ecd31af1963c5ab378bb00262ef2ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673193"
---
# <span data-ttu-id="c4beb-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c4beb-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="c4beb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4beb-102">SYNOPSIS</span></span>
<span data-ttu-id="c4beb-103">Ismerje meg az identitás-szolgáltató konfigurációjának részleteit.</span><span class="sxs-lookup"><span data-stu-id="c4beb-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4beb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4beb-104">SYNTAX</span></span>

### <span data-ttu-id="c4beb-105">AllIdentityProviders (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4beb-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4beb-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="c4beb-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4beb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4beb-107">DESCRIPTION</span></span>
<span data-ttu-id="c4beb-108">Ismerje meg az identitás-szolgáltató konfigurációjának részleteit.</span><span class="sxs-lookup"><span data-stu-id="c4beb-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="c4beb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c4beb-109">EXAMPLES</span></span>

### <span data-ttu-id="c4beb-110">1. példa: az összes személyazonosság-szolgáltató beszerzése</span><span class="sxs-lookup"><span data-stu-id="c4beb-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="c4beb-111">A szolgáltatás minden identitás-szolgáltatója konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="c4beb-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="c4beb-112">A AAD-típus identitás-szolgáltatójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="c4beb-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="c4beb-113">Az Azure Active Directory identitás-szolgáltatójának konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c4beb-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="c4beb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4beb-114">PARAMETERS</span></span>

### <span data-ttu-id="c4beb-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c4beb-115">-Context</span></span>
<span data-ttu-id="c4beb-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="c4beb-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c4beb-117">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="c4beb-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4beb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4beb-118">-DefaultProfile</span></span>
<span data-ttu-id="c4beb-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4beb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4beb-120">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="c4beb-120">-Type</span></span>
<span data-ttu-id="c4beb-121">Egy identitás-szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c4beb-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="c4beb-122">Ha meg van adva, az azonosító segítségével megpróbálja megtalálni az identitás-szolgáltató konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c4beb-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="c4beb-123">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="c4beb-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="c4beb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4beb-124">CommonParameters</span></span>
<span data-ttu-id="c4beb-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4beb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4beb-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4beb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4beb-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4beb-127">INPUTS</span></span>

### <span data-ttu-id="c4beb-128">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c4beb-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c4beb-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="c4beb-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="c4beb-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4beb-130">OUTPUTS</span></span>

### <span data-ttu-id="c4beb-131">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c4beb-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="c4beb-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4beb-132">NOTES</span></span>

## <span data-ttu-id="c4beb-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4beb-133">RELATED LINKS</span></span>
