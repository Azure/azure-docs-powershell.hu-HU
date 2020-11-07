---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c26fb8991acc47ab655cb47c44194ca209423a70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679303"
---
# <span data-ttu-id="bcb0e-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bcb0e-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="bcb0e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bcb0e-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb0e-103">Megkapja az OpenID Connect szolgáltatókat.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcb0e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bcb0e-104">SYNTAX</span></span>

### <span data-ttu-id="bcb0e-105">GetAllOpenIdConnectProviders (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bcb0e-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcb0e-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="bcb0e-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcb0e-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="bcb0e-107">GetByName</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcb0e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bcb0e-108">DESCRIPTION</span></span>
<span data-ttu-id="bcb0e-109">A **Get-AzureRmApiManagementOpenIdConnectProvider** parancsmag OpenID Connect-szolgáltatókat kap az Azure API-menedzsmentben.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="bcb0e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bcb0e-110">EXAMPLES</span></span>

### <span data-ttu-id="bcb0e-111">Példa 1: az összes szolgáltató beszerzése</span><span class="sxs-lookup"><span data-stu-id="bcb0e-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="bcb0e-112">Ez a parancs az összes OpenID Connect szolgáltatót megkapja a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="bcb0e-113">2. példa: szolgáltató beszerzése azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="bcb0e-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="bcb0e-114">Ez a parancs a OICProvicer01 AZONOSÍTÓját tartalmazó szolgáltatót kapja.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="bcb0e-115">3. példa: szolgáltató beszerzése név használatával</span><span class="sxs-lookup"><span data-stu-id="bcb0e-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="bcb0e-116">Ez a parancs a contoso OpenID Connect Provider nevű szolgáltatót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="bcb0e-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bcb0e-117">PARAMETERS</span></span>

### <span data-ttu-id="bcb0e-118">-Környezet</span><span class="sxs-lookup"><span data-stu-id="bcb0e-118">-Context</span></span>
<span data-ttu-id="bcb0e-119">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bcb0e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb0e-120">-DefaultProfile</span></span>
<span data-ttu-id="bcb0e-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="bcb0e-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bcb0e-122">-Name</span></span>
<span data-ttu-id="bcb0e-123">A szolgáltató rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="bcb0e-124">Ha megad egy nevet, ez a parancsmag a szolgáltatót kapja.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-124">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcb0e-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="bcb0e-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="bcb0e-126">Annak a szolgáltatónak az AZONOSÍTÓját adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="bcb0e-127">Ha azonosítót ad meg, ez a parancsmag a szolgáltatót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-127">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: String
Parameter Sets: GetByOpenIdConnectProviderId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcb0e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb0e-128">CommonParameters</span></span>
<span data-ttu-id="bcb0e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bcb0e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb0e-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcb0e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb0e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcb0e-131">INPUTS</span></span>

### <span data-ttu-id="bcb0e-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="bcb0e-132">None</span></span>
<span data-ttu-id="bcb0e-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bcb0e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcb0e-134">OUTPUTS</span></span>

### <span data-ttu-id="bcb0e-135">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bcb0e-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>
<span data-ttu-id="bcb0e-136">Az API-kezelési szolgáltatásban konfigurált OpenId csatlakoztatási szolgáltató részlete.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-136">The detail of the OpenId connect Provider configured in API Management service.</span></span>

### <span data-ttu-id="bcb0e-137">IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementOpenIdConnectProvider></span><span class="sxs-lookup"><span data-stu-id="bcb0e-137">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider></span></span>
<span data-ttu-id="bcb0e-138">Az API-kezelési szolgáltatásban konfigurált OpenId Connect-szolgáltatók listája.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-138">The list of OpenId Connect Providers configured in API Management service.</span></span>

## <span data-ttu-id="bcb0e-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bcb0e-139">NOTES</span></span>

## <span data-ttu-id="bcb0e-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bcb0e-140">RELATED LINKS</span></span>

[<span data-ttu-id="bcb0e-141">Új – AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bcb0e-141">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="bcb0e-142">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bcb0e-142">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="bcb0e-143">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bcb0e-143">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


