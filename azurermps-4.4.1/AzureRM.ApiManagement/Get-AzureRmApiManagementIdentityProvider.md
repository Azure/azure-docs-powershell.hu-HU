---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 2b38728f90de4639bf3e125f226ae2b40527ca45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498112"
---
# <span data-ttu-id="e849f-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="e849f-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="e849f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e849f-102">SYNOPSIS</span></span>
<span data-ttu-id="e849f-103">Ismerje meg az identitás-szolgáltató konfigurációjának részleteit.</span><span class="sxs-lookup"><span data-stu-id="e849f-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e849f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e849f-104">SYNTAX</span></span>

### <span data-ttu-id="e849f-105">AllIdentityProviders (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e849f-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e849f-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="e849f-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e849f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e849f-107">DESCRIPTION</span></span>
<span data-ttu-id="e849f-108">Ismerje meg az identitás-szolgáltató konfigurációjának részleteit.</span><span class="sxs-lookup"><span data-stu-id="e849f-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="e849f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e849f-109">EXAMPLES</span></span>

### <span data-ttu-id="e849f-110">--------------------------Példa 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e849f-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="e849f-111">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="e849f-111">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementIdentityProvider -Context $context
```

<span data-ttu-id="e849f-112">A szolgáltatás minden identitás-szolgáltatója konfigurációjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e849f-112">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="e849f-113">--------------------------Példa 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e849f-113">--------------------------  Example 2  --------------------------</span></span>
<span data-ttu-id="e849f-114">@ {bekezdés = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="e849f-114">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementIdentityProvider -Context $context -Type Aad
```

<span data-ttu-id="e849f-115">Az Azure Active Directory identitás-szolgáltatójának konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e849f-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="e849f-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e849f-116">PARAMETERS</span></span>

### <span data-ttu-id="e849f-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e849f-117">-Context</span></span>
<span data-ttu-id="e849f-118">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="e849f-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e849f-119">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="e849f-119">This parameter is required.</span></span>

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

### <span data-ttu-id="e849f-120">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="e849f-120">-Type</span></span>
<span data-ttu-id="e849f-121">Egy identitás-szolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e849f-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="e849f-122">Ha meg van adva, az azonosító segítségével megpróbálja megtalálni az identitás-szolgáltató konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="e849f-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="e849f-123">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="e849f-123">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e849f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e849f-124">-DefaultProfile</span></span>
<span data-ttu-id="e849f-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e849f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e849f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e849f-126">CommonParameters</span></span>
<span data-ttu-id="e849f-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e849f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e849f-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e849f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e849f-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e849f-129">INPUTS</span></span>

## <span data-ttu-id="e849f-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e849f-130">OUTPUTS</span></span>

### <span data-ttu-id="e849f-131">IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProvider></span><span class="sxs-lookup"><span data-stu-id="e849f-131">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider></span></span>

### <span data-ttu-id="e849f-132">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="e849f-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="e849f-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e849f-133">NOTES</span></span>

## <span data-ttu-id="e849f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e849f-134">RELATED LINKS</span></span>

