---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
ms.openlocfilehash: aecf4982b6a48ac5afca1379e1f920cfa3d6e267
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932130"
---
# <span data-ttu-id="22e1b-101">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="22e1b-101">Remove-AzApiManagementPolicy</span></span>

## <span data-ttu-id="22e1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22e1b-102">SYNOPSIS</span></span>
<span data-ttu-id="22e1b-103">Eltávolítja az API-kezelési házirendet egy adott hatókörből.</span><span class="sxs-lookup"><span data-stu-id="22e1b-103">Removes the API Management policy from a specified scope.</span></span>

## <span data-ttu-id="22e1b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="22e1b-104">SYNTAX</span></span>

### <span data-ttu-id="22e1b-105">RemoveTenantLevel (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22e1b-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22e1b-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="22e1b-106">RemoveProductLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22e1b-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="22e1b-107">RemoveApiLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22e1b-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="22e1b-108">RemoveOperationLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22e1b-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="22e1b-109">DESCRIPTION</span></span>
<span data-ttu-id="22e1b-110">A **Remove-AzApiManagementPolicy** parancsmag eltávolítja az API-kezelési házirendet a megadott hatókörből.</span><span class="sxs-lookup"><span data-stu-id="22e1b-110">The **Remove-AzApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="22e1b-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="22e1b-111">EXAMPLES</span></span>

### <span data-ttu-id="22e1b-112">1. példa: A bérlői szintű házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="22e1b-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="22e1b-113">Ez a parancs eltávolítja a bérlői szintű házirendet az API-kezelésből.</span><span class="sxs-lookup"><span data-stu-id="22e1b-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="22e1b-114">2. példa: A termékkörre vonatkozó házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="22e1b-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="22e1b-115">Ez a parancs eltávolítja a termék-hatókör házirendet az API-kezelésből.</span><span class="sxs-lookup"><span data-stu-id="22e1b-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="22e1b-116">3. példa: Az API-hatókör házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="22e1b-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="22e1b-117">Ez a parancs eltávolítja az API-hatókör házirendet az API-kezelésből.</span><span class="sxs-lookup"><span data-stu-id="22e1b-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="22e1b-118">4. példa: A művelet hatókör-házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="22e1b-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="22e1b-119">Ez a parancs eltávolítja a művelet-hatókör házirendet az API-kezelésből.</span><span class="sxs-lookup"><span data-stu-id="22e1b-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="22e1b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22e1b-120">PARAMETERS</span></span>

### <span data-ttu-id="22e1b-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="22e1b-121">-ApiId</span></span>
<span data-ttu-id="22e1b-122">Egy meglévő API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="22e1b-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="22e1b-123">Ha ezt a paramétert adja meg, a parancsmag eltávolítja az API-hatókör házirendet.</span><span class="sxs-lookup"><span data-stu-id="22e1b-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveApiLevel, RemoveOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e1b-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="22e1b-124">-Context</span></span>
<span data-ttu-id="22e1b-125">A **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="22e1b-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="22e1b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e1b-126">-DefaultProfile</span></span>
<span data-ttu-id="22e1b-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22e1b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22e1b-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="22e1b-128">-OperationId</span></span>
<span data-ttu-id="22e1b-129">Egy meglévő művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="22e1b-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="22e1b-130">Ha ezt a paramétert az *ApiId paraméterrel* adja meg, ez a parancsmag eltávolítja a művelet-hatókör házirendet.</span><span class="sxs-lookup"><span data-stu-id="22e1b-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e1b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22e1b-131">-PassThru</span></span>
<span data-ttu-id="22e1b-132">Azt jelzi, hogy ez a parancsmag $True, ha sikeres, vagy egy $False értéket.</span><span class="sxs-lookup"><span data-stu-id="22e1b-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="22e1b-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="22e1b-133">-ProductId</span></span>
<span data-ttu-id="22e1b-134">A meglévő termék azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="22e1b-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="22e1b-135">Ha ezt a paramétert adja meg, a parancsmag eltávolítja a termék-hatókör házirendet.</span><span class="sxs-lookup"><span data-stu-id="22e1b-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e1b-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22e1b-136">-Confirm</span></span>
<span data-ttu-id="22e1b-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="22e1b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22e1b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22e1b-138">-WhatIf</span></span>
<span data-ttu-id="22e1b-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="22e1b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22e1b-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22e1b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22e1b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e1b-141">CommonParameters</span></span>
<span data-ttu-id="22e1b-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22e1b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e1b-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22e1b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e1b-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22e1b-144">INPUTS</span></span>

### <span data-ttu-id="22e1b-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="22e1b-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="22e1b-146">System.String</span><span class="sxs-lookup"><span data-stu-id="22e1b-146">System.String</span></span>

### <span data-ttu-id="22e1b-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="22e1b-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="22e1b-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22e1b-148">OUTPUTS</span></span>

### <span data-ttu-id="22e1b-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="22e1b-149">System.Boolean</span></span>

## <span data-ttu-id="22e1b-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="22e1b-150">NOTES</span></span>

## <span data-ttu-id="22e1b-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22e1b-151">RELATED LINKS</span></span>

[<span data-ttu-id="22e1b-152">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="22e1b-152">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="22e1b-153">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="22e1b-153">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


