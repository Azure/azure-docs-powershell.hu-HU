---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: ee1ac7cda19f2b37ac1313d30075aa9c620bbd54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503127"
---
# <span data-ttu-id="b6fa2-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b6fa2-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="b6fa2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6fa2-102">SYNOPSIS</span></span>
<span data-ttu-id="b6fa2-103">Egy OpenID csatlakoztatási szolgáltató eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b6fa2-103">Removes an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6fa2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6fa2-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6fa2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6fa2-105">DESCRIPTION</span></span>
<span data-ttu-id="b6fa2-106">A **Remove-AzureRmApiManagementOpenIdConnectProvider** parancsmag egy OpenID Connect szolgáltatót távolít el az Azure API-kezeléshez.</span><span class="sxs-lookup"><span data-stu-id="b6fa2-106">The **Remove-AzureRmApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="b6fa2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b6fa2-107">EXAMPLES</span></span>

### <span data-ttu-id="b6fa2-108">1. példa: szolgáltató eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b6fa2-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -PassThru
```

<span data-ttu-id="b6fa2-109">Ez a parancs eltávolítja azt a szolgáltatót, amely az azonosító OICProvicer01 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b6fa2-109">This command removes a provider that has the ID OICProvicer01.</span></span>

## <span data-ttu-id="b6fa2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6fa2-110">PARAMETERS</span></span>

### <span data-ttu-id="b6fa2-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b6fa2-111">-Context</span></span>
<span data-ttu-id="b6fa2-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b6fa2-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b6fa2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6fa2-113">-DefaultProfile</span></span>
<span data-ttu-id="b6fa2-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6fa2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="b6fa2-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="b6fa2-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="b6fa2-116">Annak a szolgáltatónak az AZONOSÍTÓját adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="b6fa2-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6fa2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6fa2-117">-PassThru</span></span>
<span data-ttu-id="b6fa2-118">Azt jelzi, hogy ez a parancsmag $True értéket ad eredményül, ha a művelet sikerül vagy $False más módon.</span><span class="sxs-lookup"><span data-stu-id="b6fa2-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6fa2-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b6fa2-119">-Confirm</span></span>
<span data-ttu-id="b6fa2-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6fa2-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6fa2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6fa2-121">-WhatIf</span></span>
<span data-ttu-id="b6fa2-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6fa2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6fa2-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6fa2-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6fa2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6fa2-124">CommonParameters</span></span>
<span data-ttu-id="b6fa2-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6fa2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6fa2-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6fa2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6fa2-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6fa2-127">INPUTS</span></span>

### <span data-ttu-id="b6fa2-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="b6fa2-128">None</span></span>
<span data-ttu-id="b6fa2-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b6fa2-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b6fa2-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6fa2-130">OUTPUTS</span></span>

### <span data-ttu-id="b6fa2-131">Logikai</span><span class="sxs-lookup"><span data-stu-id="b6fa2-131">Boolean</span></span>

## <span data-ttu-id="b6fa2-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6fa2-132">NOTES</span></span>

## <span data-ttu-id="b6fa2-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6fa2-133">RELATED LINKS</span></span>

[<span data-ttu-id="b6fa2-134">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b6fa2-134">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="b6fa2-135">Új – AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b6fa2-135">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="b6fa2-136">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b6fa2-136">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


