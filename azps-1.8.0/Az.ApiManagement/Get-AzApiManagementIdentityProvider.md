---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: fe23034b6fc86c9aa76629f806dcb406608f456c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665684"
---
# <span data-ttu-id="ac76f-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ac76f-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="ac76f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac76f-102">SYNOPSIS</span></span>
<span data-ttu-id="ac76f-103">Ismerje meg az identitás-szolgáltató konfigurációjának részleteit.</span><span class="sxs-lookup"><span data-stu-id="ac76f-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="ac76f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac76f-104">SYNTAX</span></span>

### <span data-ttu-id="ac76f-105">AllIdentityProviders (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ac76f-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac76f-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="ac76f-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac76f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac76f-107">DESCRIPTION</span></span>
<span data-ttu-id="ac76f-108">Ismerje meg az identitás-szolgáltató konfigurációjának részleteit.</span><span class="sxs-lookup"><span data-stu-id="ac76f-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="ac76f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ac76f-109">EXAMPLES</span></span>

### <span data-ttu-id="ac76f-110">1. példa: az összes személyazonosság-szolgáltató beszerzése</span><span class="sxs-lookup"><span data-stu-id="ac76f-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="ac76f-111">A szolgáltatás minden identitás-szolgáltatója konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ac76f-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="ac76f-112">A AAD-típus identitás-szolgáltatójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ac76f-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="ac76f-113">Az Azure Active Directory identitás-szolgáltatójának konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ac76f-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="ac76f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac76f-114">PARAMETERS</span></span>

### <span data-ttu-id="ac76f-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ac76f-115">-Context</span></span>
<span data-ttu-id="ac76f-116">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="ac76f-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ac76f-117">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ac76f-117">This parameter is required.</span></span>

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

### <span data-ttu-id="ac76f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac76f-118">-DefaultProfile</span></span>
<span data-ttu-id="ac76f-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac76f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac76f-120">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="ac76f-120">-Type</span></span>
<span data-ttu-id="ac76f-121">Egy identitás-szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ac76f-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="ac76f-122">Ha meg van adva, az azonosító segítségével megpróbálja megtalálni az identitás-szolgáltató konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="ac76f-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="ac76f-123">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ac76f-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="ac76f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac76f-124">CommonParameters</span></span>
<span data-ttu-id="ac76f-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac76f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac76f-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac76f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac76f-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac76f-127">INPUTS</span></span>

### <span data-ttu-id="ac76f-128">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ac76f-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ac76f-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="ac76f-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="ac76f-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac76f-130">OUTPUTS</span></span>

### <span data-ttu-id="ac76f-131">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ac76f-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="ac76f-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac76f-132">NOTES</span></span>

## <span data-ttu-id="ac76f-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac76f-133">RELATED LINKS</span></span>
