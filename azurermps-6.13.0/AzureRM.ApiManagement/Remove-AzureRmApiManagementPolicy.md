---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 1066598a9e255cecbf7238208b5f06f74d88511e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495190"
---
# <span data-ttu-id="ebf2c-101">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ebf2c-101">Remove-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="ebf2c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ebf2c-102">SYNOPSIS</span></span>
<span data-ttu-id="ebf2c-103">Eltávolítja az API-kezelési házirendet egy megadott hatókörből.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-103">Removes the API Management policy from a specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebf2c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ebf2c-104">SYNTAX</span></span>

### <span data-ttu-id="ebf2c-105">RemoveTenantLevel (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ebf2c-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebf2c-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="ebf2c-106">RemoveProductLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebf2c-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="ebf2c-107">RemoveApiLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebf2c-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="ebf2c-108">RemoveOperationLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebf2c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="ebf2c-109">DESCRIPTION</span></span>
<span data-ttu-id="ebf2c-110">A **Remove-AzureRmApiManagementPolicy** parancsmag meghatározott hatókörből ELTÁVOLÍTJA az API-kezelési házirendet.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-110">The **Remove-AzureRmApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="ebf2c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ebf2c-111">EXAMPLES</span></span>

### <span data-ttu-id="ebf2c-112">1. példa: a bérlői szintű házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ebf2c-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="ebf2c-113">Ez a parancs eltávolítja a bérlői szintű házirendet az API-menedzsmentből.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="ebf2c-114">2. példa: a termékskála-házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ebf2c-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="ebf2c-115">Ez a parancs az API-kezelésből eltávolítja a termékskála-házirendet.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="ebf2c-116">3. példa: az API-scope-házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ebf2c-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="ebf2c-117">Ez a parancs eltávolítja az API-scope-házirendet az API-menedzsmentből.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="ebf2c-118">4. példa: a műveleti hatókörű házirend eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ebf2c-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="ebf2c-119">Ez a parancs eltávolítja a műveleti hatóköri házirendet az API-kezelésből.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="ebf2c-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ebf2c-120">PARAMETERS</span></span>

### <span data-ttu-id="ebf2c-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ebf2c-121">-ApiId</span></span>
<span data-ttu-id="ebf2c-122">Egy meglévő API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="ebf2c-123">Ha ezt a paramétert adja meg, a parancsmag eltávolítja az API-scope-házirendet.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

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

### <span data-ttu-id="ebf2c-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ebf2c-124">-Context</span></span>
<span data-ttu-id="ebf2c-125">A **PsApiManagementContext** objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ebf2c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebf2c-126">-DefaultProfile</span></span>
<span data-ttu-id="ebf2c-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebf2c-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ebf2c-128">-OperationId</span></span>
<span data-ttu-id="ebf2c-129">Egy meglévő művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="ebf2c-130">Ha a *ApiId* paraméterrel adja meg ezt a paramétert, ez a parancsmag eltávolítja a művelet-hatóköri házirendet.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

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

### <span data-ttu-id="ebf2c-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebf2c-131">-PassThru</span></span>
<span data-ttu-id="ebf2c-132">Azt jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy ha az $False értéke más.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="ebf2c-133">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="ebf2c-133">-ProductId</span></span>
<span data-ttu-id="ebf2c-134">A meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="ebf2c-135">Ha ezt a paramétert adja meg, a parancsmag eltávolítja a Product-scope-házirendet.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

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

### <span data-ttu-id="ebf2c-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ebf2c-136">-Confirm</span></span>
<span data-ttu-id="ebf2c-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebf2c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebf2c-138">-WhatIf</span></span>
<span data-ttu-id="ebf2c-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebf2c-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ebf2c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebf2c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebf2c-141">CommonParameters</span></span>
<span data-ttu-id="ebf2c-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ebf2c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebf2c-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebf2c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebf2c-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebf2c-144">INPUTS</span></span>

### <span data-ttu-id="ebf2c-145">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ebf2c-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ebf2c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="ebf2c-146">System.String</span></span>

### <span data-ttu-id="ebf2c-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ebf2c-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ebf2c-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebf2c-148">OUTPUTS</span></span>

### <span data-ttu-id="ebf2c-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ebf2c-149">System.Boolean</span></span>

## <span data-ttu-id="ebf2c-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ebf2c-150">NOTES</span></span>

## <span data-ttu-id="ebf2c-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ebf2c-151">RELATED LINKS</span></span>

[<span data-ttu-id="ebf2c-152">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ebf2c-152">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="ebf2c-153">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ebf2c-153">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


