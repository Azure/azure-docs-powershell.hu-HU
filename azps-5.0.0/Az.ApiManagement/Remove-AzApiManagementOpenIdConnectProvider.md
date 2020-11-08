---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: ab278dcf56646463e1ccbc8ada9baa896b1759bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187861"
---
# <span data-ttu-id="bc3e1-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bc3e1-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="bc3e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc3e1-102">SYNOPSIS</span></span>
<span data-ttu-id="bc3e1-103">Egy OpenID csatlakoztatási szolgáltató eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="bc3e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc3e1-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc3e1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc3e1-105">DESCRIPTION</span></span>
<span data-ttu-id="bc3e1-106">A **Remove-AzApiManagementOpenIdConnectProvider** parancsmag egy OpenID Connect szolgáltatót távolít el az Azure API-kezeléshez.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="bc3e1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bc3e1-107">EXAMPLES</span></span>

### <span data-ttu-id="bc3e1-108">1. példa: szolgáltató eltávolítása</span><span class="sxs-lookup"><span data-stu-id="bc3e1-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="bc3e1-109">Ez a parancs eltávolítja azt a szolgáltatót, amely az azonosító OICProvider01 tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="bc3e1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc3e1-110">PARAMETERS</span></span>

### <span data-ttu-id="bc3e1-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="bc3e1-111">-Context</span></span>
<span data-ttu-id="bc3e1-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bc3e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc3e1-113">-DefaultProfile</span></span>
<span data-ttu-id="bc3e1-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc3e1-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="bc3e1-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="bc3e1-116">Annak a szolgáltatónak az AZONOSÍTÓját adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bc3e1-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc3e1-117">-PassThru</span></span>
<span data-ttu-id="bc3e1-118">Azt jelzi, hogy ez a parancsmag $True értéket ad eredményül, ha a művelet sikerül vagy $False más módon.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="bc3e1-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bc3e1-119">-Confirm</span></span>
<span data-ttu-id="bc3e1-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc3e1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc3e1-121">-WhatIf</span></span>
<span data-ttu-id="bc3e1-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc3e1-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc3e1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc3e1-124">CommonParameters</span></span>
<span data-ttu-id="bc3e1-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc3e1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc3e1-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bc3e1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc3e1-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc3e1-127">INPUTS</span></span>

### <span data-ttu-id="bc3e1-128">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bc3e1-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bc3e1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bc3e1-129">System.String</span></span>

### <span data-ttu-id="bc3e1-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bc3e1-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bc3e1-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc3e1-131">OUTPUTS</span></span>

### <span data-ttu-id="bc3e1-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bc3e1-132">System.Boolean</span></span>

## <span data-ttu-id="bc3e1-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc3e1-133">NOTES</span></span>

## <span data-ttu-id="bc3e1-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc3e1-134">RELATED LINKS</span></span>

[<span data-ttu-id="bc3e1-135">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bc3e1-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="bc3e1-136">Új – AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bc3e1-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="bc3e1-137">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bc3e1-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


