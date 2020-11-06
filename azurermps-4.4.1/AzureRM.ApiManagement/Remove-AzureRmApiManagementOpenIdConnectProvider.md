---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 686b988ef5bf62e5eed7e4f8fae94f6b29b1b4ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493888"
---
# <span data-ttu-id="02ffd-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="02ffd-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="02ffd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02ffd-102">SYNOPSIS</span></span>
<span data-ttu-id="02ffd-103">Egy OpenID csatlakoztatási szolgáltató eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="02ffd-103">Removes an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02ffd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02ffd-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02ffd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="02ffd-105">DESCRIPTION</span></span>
<span data-ttu-id="02ffd-106">A **Remove-AzureRmApiManagementOpenIdConnectProvider** parancsmag egy OpenID Connect szolgáltatót távolít el az Azure API-kezeléshez.</span><span class="sxs-lookup"><span data-stu-id="02ffd-106">The **Remove-AzureRmApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="02ffd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="02ffd-107">EXAMPLES</span></span>

### <span data-ttu-id="02ffd-108">1. példa: szolgáltató eltávolítása</span><span class="sxs-lookup"><span data-stu-id="02ffd-108">Example 1: Remove a provider</span></span>
```
PS C:\>Remove-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -PassThru
```

<span data-ttu-id="02ffd-109">Ez a parancs eltávolítja azt a szolgáltatót, amely az azonosító OICProvicer01 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="02ffd-109">This command removes a provider that has the ID OICProvicer01.</span></span>

## <span data-ttu-id="02ffd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02ffd-110">PARAMETERS</span></span>

### <span data-ttu-id="02ffd-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="02ffd-111">-Context</span></span>
<span data-ttu-id="02ffd-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="02ffd-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="02ffd-113">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="02ffd-113">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="02ffd-114">Annak a szolgáltatónak az AZONOSÍTÓját adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="02ffd-114">Specifies an ID of the provider that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02ffd-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02ffd-115">-PassThru</span></span>
<span data-ttu-id="02ffd-116">Azt jelzi, hogy ez a parancsmag $True értéket ad eredményül, ha a művelet sikerül vagy $False más módon.</span><span class="sxs-lookup"><span data-stu-id="02ffd-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02ffd-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="02ffd-117">-Confirm</span></span>
<span data-ttu-id="02ffd-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="02ffd-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ffd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02ffd-119">-WhatIf</span></span>
<span data-ttu-id="02ffd-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="02ffd-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02ffd-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="02ffd-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ffd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02ffd-122">-DefaultProfile</span></span>
<span data-ttu-id="02ffd-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02ffd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02ffd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ffd-124">CommonParameters</span></span>
<span data-ttu-id="02ffd-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02ffd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ffd-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02ffd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ffd-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02ffd-127">INPUTS</span></span>

## <span data-ttu-id="02ffd-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02ffd-128">OUTPUTS</span></span>

### <span data-ttu-id="02ffd-129">Logikai</span><span class="sxs-lookup"><span data-stu-id="02ffd-129">Boolean</span></span>

## <span data-ttu-id="02ffd-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02ffd-130">NOTES</span></span>

## <span data-ttu-id="02ffd-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02ffd-131">RELATED LINKS</span></span>

[<span data-ttu-id="02ffd-132">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="02ffd-132">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="02ffd-133">Új – AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="02ffd-133">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="02ffd-134">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="02ffd-134">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


