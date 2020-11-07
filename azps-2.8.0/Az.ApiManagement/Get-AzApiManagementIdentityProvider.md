---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: f3692383f5fc93c0d76951f6dcaeb409ae3ee0f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668108"
---
# <span data-ttu-id="de6ee-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="de6ee-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="de6ee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de6ee-102">SYNOPSIS</span></span>
<span data-ttu-id="de6ee-103">Ismerje meg az identitás-szolgáltató konfigurációjának részleteit.</span><span class="sxs-lookup"><span data-stu-id="de6ee-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="de6ee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de6ee-104">SYNTAX</span></span>

### <span data-ttu-id="de6ee-105">AllIdentityProviders (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="de6ee-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de6ee-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="de6ee-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de6ee-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="de6ee-107">DESCRIPTION</span></span>
<span data-ttu-id="de6ee-108">Ismerje meg az identitás-szolgáltató konfigurációjának részleteit.</span><span class="sxs-lookup"><span data-stu-id="de6ee-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="de6ee-109">Példák</span><span class="sxs-lookup"><span data-stu-id="de6ee-109">EXAMPLES</span></span>

### <span data-ttu-id="de6ee-110">1. példa: az összes személyazonosság-szolgáltató beszerzése</span><span class="sxs-lookup"><span data-stu-id="de6ee-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="de6ee-111">A szolgáltatás minden identitás-szolgáltatója konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="de6ee-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="de6ee-112">A AAD-típus identitás-szolgáltatójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="de6ee-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="de6ee-113">Az Azure Active Directory identitás-szolgáltatójának konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="de6ee-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="de6ee-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de6ee-114">PARAMETERS</span></span>

### <span data-ttu-id="de6ee-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="de6ee-115">-Context</span></span>
<span data-ttu-id="de6ee-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="de6ee-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="de6ee-117">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="de6ee-117">This parameter is required.</span></span>

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

### <span data-ttu-id="de6ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de6ee-118">-DefaultProfile</span></span>
<span data-ttu-id="de6ee-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de6ee-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de6ee-120">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="de6ee-120">-Type</span></span>
<span data-ttu-id="de6ee-121">Egy identitás-szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="de6ee-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="de6ee-122">Ha meg van adva, az azonosító segítségével megpróbálja megtalálni az identitás-szolgáltató konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="de6ee-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="de6ee-123">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="de6ee-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="de6ee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de6ee-124">CommonParameters</span></span>
<span data-ttu-id="de6ee-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de6ee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de6ee-126">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="de6ee-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de6ee-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de6ee-127">INPUTS</span></span>

### <span data-ttu-id="de6ee-128">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="de6ee-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="de6ee-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="de6ee-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="de6ee-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de6ee-130">OUTPUTS</span></span>

### <span data-ttu-id="de6ee-131">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="de6ee-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="de6ee-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de6ee-132">NOTES</span></span>

## <span data-ttu-id="de6ee-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de6ee-133">RELATED LINKS</span></span>
