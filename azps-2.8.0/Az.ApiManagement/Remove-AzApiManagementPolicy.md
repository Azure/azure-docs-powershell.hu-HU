---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
ms.openlocfilehash: c4f2ce8db3a799ad3d49d1c967da93a8fea93a39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667977"
---
# <span data-ttu-id="b3012-101">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b3012-101">Remove-AzApiManagementPolicy</span></span>

## <span data-ttu-id="b3012-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b3012-102">SYNOPSIS</span></span>
<span data-ttu-id="b3012-103">Eltávolítja az API-kezelési házirendet egy megadott hatókörből.</span><span class="sxs-lookup"><span data-stu-id="b3012-103">Removes the API Management policy from a specified scope.</span></span>

## <span data-ttu-id="b3012-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b3012-104">SYNTAX</span></span>

### <span data-ttu-id="b3012-105">RemoveTenantLevel (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b3012-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3012-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="b3012-106">RemoveProductLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3012-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="b3012-107">RemoveApiLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3012-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="b3012-108">RemoveOperationLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3012-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="b3012-109">DESCRIPTION</span></span>
<span data-ttu-id="b3012-110">A **Remove-AzApiManagementPolicy** parancsmag meghatározott hatókörből ELTÁVOLÍTJA az API-kezelési házirendet.</span><span class="sxs-lookup"><span data-stu-id="b3012-110">The **Remove-AzApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="b3012-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b3012-111">EXAMPLES</span></span>

### <span data-ttu-id="b3012-112">1. példa: a bérlői szintű házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b3012-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="b3012-113">Ez a parancs eltávolítja a bérlői szintű házirendet az API-menedzsmentből.</span><span class="sxs-lookup"><span data-stu-id="b3012-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="b3012-114">2. példa: a termékskála-házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b3012-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="b3012-115">Ez a parancs az API-kezelésből eltávolítja a termékskála-házirendet.</span><span class="sxs-lookup"><span data-stu-id="b3012-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="b3012-116">3. példa: az API-scope-házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b3012-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="b3012-117">Ez a parancs eltávolítja az API-scope-házirendet az API-menedzsmentből.</span><span class="sxs-lookup"><span data-stu-id="b3012-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="b3012-118">4. példa: a műveleti hatókörű házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b3012-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="b3012-119">Ez a parancs eltávolítja a műveleti hatóköri házirendet az API-kezelésből.</span><span class="sxs-lookup"><span data-stu-id="b3012-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="b3012-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b3012-120">PARAMETERS</span></span>

### <span data-ttu-id="b3012-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b3012-121">-ApiId</span></span>
<span data-ttu-id="b3012-122">Egy meglévő API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3012-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="b3012-123">Ha ezt a paramétert adja meg, a parancsmag eltávolítja az API-scope-házirendet.</span><span class="sxs-lookup"><span data-stu-id="b3012-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

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

### <span data-ttu-id="b3012-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b3012-124">-Context</span></span>
<span data-ttu-id="b3012-125">A **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3012-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b3012-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3012-126">-DefaultProfile</span></span>
<span data-ttu-id="b3012-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b3012-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3012-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="b3012-128">-OperationId</span></span>
<span data-ttu-id="b3012-129">Egy meglévő művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3012-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="b3012-130">Ha a *ApiId* paraméterrel adja meg ezt a paramétert, ez a parancsmag eltávolítja a művelet-hatóköri házirendet.</span><span class="sxs-lookup"><span data-stu-id="b3012-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

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

### <span data-ttu-id="b3012-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3012-131">-PassThru</span></span>
<span data-ttu-id="b3012-132">Azt jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy ha az $False értéke más.</span><span class="sxs-lookup"><span data-stu-id="b3012-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="b3012-133">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="b3012-133">-ProductId</span></span>
<span data-ttu-id="b3012-134">A meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3012-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="b3012-135">Ha ezt a paramétert adja meg, a parancsmag eltávolítja a Product-scope-házirendet.</span><span class="sxs-lookup"><span data-stu-id="b3012-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

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

### <span data-ttu-id="b3012-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b3012-136">-Confirm</span></span>
<span data-ttu-id="b3012-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b3012-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3012-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3012-138">-WhatIf</span></span>
<span data-ttu-id="b3012-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b3012-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3012-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b3012-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3012-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3012-141">CommonParameters</span></span>
<span data-ttu-id="b3012-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b3012-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3012-143">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b3012-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3012-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3012-144">INPUTS</span></span>

### <span data-ttu-id="b3012-145">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b3012-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b3012-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b3012-146">System.String</span></span>

### <span data-ttu-id="b3012-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b3012-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b3012-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3012-148">OUTPUTS</span></span>

### <span data-ttu-id="b3012-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b3012-149">System.Boolean</span></span>

## <span data-ttu-id="b3012-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b3012-150">NOTES</span></span>

## <span data-ttu-id="b3012-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3012-151">RELATED LINKS</span></span>

[<span data-ttu-id="b3012-152">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b3012-152">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="b3012-153">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b3012-153">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


