---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: e25e3bfad6c40b136c3cbaa65999b8118e0abd11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500631"
---
# <span data-ttu-id="605d8-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="605d8-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="605d8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="605d8-102">SYNOPSIS</span></span>
<span data-ttu-id="605d8-103">Ismerje meg az identitás-szolgáltató konfigurációjának részleteit.</span><span class="sxs-lookup"><span data-stu-id="605d8-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="605d8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="605d8-104">SYNTAX</span></span>

### <span data-ttu-id="605d8-105">AllIdentityProviders (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="605d8-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="605d8-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="605d8-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="605d8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="605d8-107">DESCRIPTION</span></span>
<span data-ttu-id="605d8-108">Ismerje meg az identitás-szolgáltató konfigurációjának részleteit.</span><span class="sxs-lookup"><span data-stu-id="605d8-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="605d8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="605d8-109">EXAMPLES</span></span>

### <span data-ttu-id="605d8-110">1. példa: az összes személyazonosság-szolgáltató beszerzése</span><span class="sxs-lookup"><span data-stu-id="605d8-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="605d8-111">A szolgáltatás minden identitás-szolgáltatója konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="605d8-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="605d8-112">A AAD-típus identitás-szolgáltatójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="605d8-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="605d8-113">Az Azure Active Directory identitás-szolgáltatójának konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="605d8-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="605d8-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="605d8-114">PARAMETERS</span></span>

### <span data-ttu-id="605d8-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="605d8-115">-Context</span></span>
<span data-ttu-id="605d8-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="605d8-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="605d8-117">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="605d8-117">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="605d8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="605d8-118">-DefaultProfile</span></span>
<span data-ttu-id="605d8-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="605d8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="605d8-120">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="605d8-120">-Type</span></span>
<span data-ttu-id="605d8-121">Egy identitás-szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="605d8-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="605d8-122">Ha meg van adva, az azonosító segítségével megpróbálja megtalálni az identitás-szolgáltató konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="605d8-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="605d8-123">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="605d8-123">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="605d8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="605d8-124">CommonParameters</span></span>
<span data-ttu-id="605d8-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="605d8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="605d8-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="605d8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="605d8-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="605d8-127">INPUTS</span></span>

### <span data-ttu-id="605d8-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="605d8-128">None</span></span>
<span data-ttu-id="605d8-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="605d8-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="605d8-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="605d8-130">OUTPUTS</span></span>

### <span data-ttu-id="605d8-131">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="605d8-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>
<span data-ttu-id="605d8-132">Az adatszolgáltató API-kezelési szolgáltatásban konfigurált adatai.</span><span class="sxs-lookup"><span data-stu-id="605d8-132">The details of the Identity Provider configured in API Management service.</span></span>

### <span data-ttu-id="605d8-133">IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProvider></span><span class="sxs-lookup"><span data-stu-id="605d8-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider></span></span>
<span data-ttu-id="605d8-134">Az API-kezelési szolgáltatásban konfigurált Identitáskezelő-szolgáltatók listája.</span><span class="sxs-lookup"><span data-stu-id="605d8-134">The list of Identity Providers configured in API Management service.</span></span>

## <span data-ttu-id="605d8-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="605d8-135">NOTES</span></span>

## <span data-ttu-id="605d8-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="605d8-136">RELATED LINKS</span></span>

