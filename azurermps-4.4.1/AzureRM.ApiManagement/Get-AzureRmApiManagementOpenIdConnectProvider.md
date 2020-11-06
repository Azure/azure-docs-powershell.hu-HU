---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: d97090f6374890d9ae7ba24e53d6e1d60430f7b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492619"
---
# <span data-ttu-id="6a024-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="6a024-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="6a024-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a024-102">SYNOPSIS</span></span>
<span data-ttu-id="6a024-103">Megkapja az OpenID Connect szolgáltatókat.</span><span class="sxs-lookup"><span data-stu-id="6a024-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a024-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a024-104">SYNTAX</span></span>

### <span data-ttu-id="6a024-105">Az összes OpenID Connect-szolgáltató beszerzése (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6a024-105">Get all OpenID Connect Providers (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a024-106">Get by OpenID Connect Provider azonosító</span><span class="sxs-lookup"><span data-stu-id="6a024-106">Get by OpenID Connect Provider ID</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a024-107">Keresés az OpenID-kapcsolat szolgáltatójának felhasználóbarát nevében</span><span class="sxs-lookup"><span data-stu-id="6a024-107">Find by OpenID Connect Provider friendly Name</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a024-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a024-108">DESCRIPTION</span></span>
<span data-ttu-id="6a024-109">A **Get-AzureRmApiManagementOpenIdConnectProvider** parancsmag OpenID Connect-szolgáltatókat kap az Azure API-menedzsmentben.</span><span class="sxs-lookup"><span data-stu-id="6a024-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="6a024-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6a024-110">EXAMPLES</span></span>

### <span data-ttu-id="6a024-111">Példa 1: az összes szolgáltató beszerzése</span><span class="sxs-lookup"><span data-stu-id="6a024-111">Example 1: Get all providers</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext
```

<span data-ttu-id="6a024-112">Ez a parancs az összes OpenID Connect szolgáltatót megkapja a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="6a024-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="6a024-113">2. példa: szolgáltató beszerzése azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="6a024-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="6a024-114">Ez a parancs a OICProvicer01 AZONOSÍTÓját tartalmazó szolgáltatót kapja.</span><span class="sxs-lookup"><span data-stu-id="6a024-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="6a024-115">3. példa: szolgáltató beszerzése név használatával</span><span class="sxs-lookup"><span data-stu-id="6a024-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="6a024-116">Ez a parancs a contoso OpenID Connect Provider nevű szolgáltatót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6a024-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="6a024-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a024-117">PARAMETERS</span></span>

### <span data-ttu-id="6a024-118">-Környezet</span><span class="sxs-lookup"><span data-stu-id="6a024-118">-Context</span></span>
<span data-ttu-id="6a024-119">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6a024-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6a024-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6a024-120">-Name</span></span>
<span data-ttu-id="6a024-121">A szolgáltató rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a024-121">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="6a024-122">Ha megad egy nevet, ez a parancsmag a szolgáltatót kapja.</span><span class="sxs-lookup"><span data-stu-id="6a024-122">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by OpenID Connect Provider friendly Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a024-123">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="6a024-123">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="6a024-124">Annak a szolgáltatónak az AZONOSÍTÓját adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="6a024-124">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="6a024-125">Ha azonosítót ad meg, ez a parancsmag a szolgáltatót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6a024-125">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by OpenID Connect Provider ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a024-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a024-126">-DefaultProfile</span></span>
<span data-ttu-id="6a024-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a024-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a024-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a024-128">CommonParameters</span></span>
<span data-ttu-id="6a024-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a024-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a024-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a024-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a024-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a024-131">INPUTS</span></span>

## <span data-ttu-id="6a024-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a024-132">OUTPUTS</span></span>

### <span data-ttu-id="6a024-133">IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOpenIdConnectProvider></span><span class="sxs-lookup"><span data-stu-id="6a024-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider></span></span>

## <span data-ttu-id="6a024-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a024-134">NOTES</span></span>

## <span data-ttu-id="6a024-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a024-135">RELATED LINKS</span></span>

[<span data-ttu-id="6a024-136">Új – AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="6a024-136">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="6a024-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="6a024-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="6a024-138">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="6a024-138">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


