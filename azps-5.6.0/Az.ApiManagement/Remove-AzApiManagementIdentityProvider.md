---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: f80fe2b09be6d4bdc624f65de014d3b7f1beadd6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015526"
---
# <span data-ttu-id="b32de-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b32de-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="b32de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b32de-102">SYNOPSIS</span></span>
<span data-ttu-id="b32de-103">Eltávolít egy meglévő identitásszolgáltató-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="b32de-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="b32de-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b32de-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b32de-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b32de-105">DESCRIPTION</span></span>
<span data-ttu-id="b32de-106">Eltávolít egy meglévő identitásszolgáltató-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="b32de-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="b32de-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b32de-107">EXAMPLES</span></span>

### <span data-ttu-id="b32de-108">1. példa: A Facebook-identitásszolgáltató beállításainak eltávolítása az ApiManagement szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="b32de-108">Example 1: Removes the Facebook identity provider settings from ApiManagement service</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="b32de-109">Törli a Facebook-identitásszolgáltató konfigurációjával kapcsolatos konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="b32de-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="b32de-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b32de-110">PARAMETERS</span></span>

### <span data-ttu-id="b32de-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b32de-111">-Context</span></span>
<span data-ttu-id="b32de-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="b32de-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b32de-113">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="b32de-113">This parameter is required.</span></span>

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

### <span data-ttu-id="b32de-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b32de-114">-DefaultProfile</span></span>
<span data-ttu-id="b32de-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b32de-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b32de-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b32de-116">-PassThru</span></span>
<span data-ttu-id="b32de-117">Azt jelzi, hogy ez a parancsmag visszatérési értéke $True, ha a művelet sikeres, $False egyéb esetben.</span><span class="sxs-lookup"><span data-stu-id="b32de-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="b32de-118">-Type</span><span class="sxs-lookup"><span data-stu-id="b32de-118">-Type</span></span>
<span data-ttu-id="b32de-119">Egy meglévő identitásszolgáltató azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b32de-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="b32de-120">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="b32de-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b32de-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b32de-121">-Confirm</span></span>
<span data-ttu-id="b32de-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b32de-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b32de-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b32de-123">-WhatIf</span></span>
<span data-ttu-id="b32de-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b32de-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b32de-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b32de-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b32de-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b32de-126">CommonParameters</span></span>
<span data-ttu-id="b32de-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b32de-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b32de-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b32de-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b32de-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b32de-129">INPUTS</span></span>

### <span data-ttu-id="b32de-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b32de-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b32de-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="b32de-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="b32de-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b32de-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b32de-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b32de-133">OUTPUTS</span></span>

### <span data-ttu-id="b32de-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b32de-134">System.Boolean</span></span>

## <span data-ttu-id="b32de-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b32de-135">NOTES</span></span>

## <span data-ttu-id="b32de-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b32de-136">RELATED LINKS</span></span>

[<span data-ttu-id="b32de-137">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b32de-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="b32de-138">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b32de-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="b32de-139">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b32de-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)

