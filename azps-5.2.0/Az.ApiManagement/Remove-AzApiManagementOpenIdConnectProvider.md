---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: ab278dcf56646463e1ccbc8ada9baa896b1759bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361337"
---
# <span data-ttu-id="5cc50-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5cc50-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="5cc50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cc50-102">SYNOPSIS</span></span>
<span data-ttu-id="5cc50-103">Eltávolít egy OpenID Connect-szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="5cc50-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="5cc50-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5cc50-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cc50-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5cc50-105">DESCRIPTION</span></span>
<span data-ttu-id="5cc50-106">A **Remove-AzApiManagementOpenIdConnectProvider** parancsmag eltávolít egy OpenID Connect-szolgáltatót az Azure API-kezeléshez.</span><span class="sxs-lookup"><span data-stu-id="5cc50-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="5cc50-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5cc50-107">EXAMPLES</span></span>

### <span data-ttu-id="5cc50-108">1. példa: Szolgáltató eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5cc50-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="5cc50-109">Ez a parancs eltávolít egy OICProvider01 azonosítójú szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="5cc50-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="5cc50-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cc50-110">PARAMETERS</span></span>

### <span data-ttu-id="5cc50-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5cc50-111">-Context</span></span>
<span data-ttu-id="5cc50-112">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="5cc50-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5cc50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cc50-113">-DefaultProfile</span></span>
<span data-ttu-id="5cc50-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5cc50-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cc50-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="5cc50-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="5cc50-116">Megadja annak a szolgáltatónak az azonosítóját, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="5cc50-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5cc50-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5cc50-117">-PassThru</span></span>
<span data-ttu-id="5cc50-118">Azt jelzi, hogy ez a parancsmag visszatérési értéke $True, ha a művelet sikeres, $False egyéb esetben.</span><span class="sxs-lookup"><span data-stu-id="5cc50-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="5cc50-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cc50-119">-Confirm</span></span>
<span data-ttu-id="5cc50-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5cc50-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cc50-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cc50-121">-WhatIf</span></span>
<span data-ttu-id="5cc50-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5cc50-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cc50-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5cc50-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cc50-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cc50-124">CommonParameters</span></span>
<span data-ttu-id="5cc50-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cc50-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cc50-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5cc50-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cc50-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5cc50-127">INPUTS</span></span>

### <span data-ttu-id="5cc50-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5cc50-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5cc50-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5cc50-129">System.String</span></span>

### <span data-ttu-id="5cc50-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5cc50-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5cc50-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cc50-131">OUTPUTS</span></span>

### <span data-ttu-id="5cc50-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5cc50-132">System.Boolean</span></span>

## <span data-ttu-id="5cc50-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5cc50-133">NOTES</span></span>

## <span data-ttu-id="5cc50-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5cc50-134">RELATED LINKS</span></span>

[<span data-ttu-id="5cc50-135">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5cc50-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="5cc50-136">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5cc50-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="5cc50-137">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5cc50-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


