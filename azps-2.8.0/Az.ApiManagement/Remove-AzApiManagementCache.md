---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: a95be9f18c00d72afb6117d1689f62a6bad053b4
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398682"
---
# <span data-ttu-id="9ae5a-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="9ae5a-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="9ae5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ae5a-102">SYNOPSIS</span></span>
<span data-ttu-id="9ae5a-103">Eltávolítja a gyorsítótárattitást.</span><span class="sxs-lookup"><span data-stu-id="9ae5a-103">Removes the cache entity.</span></span>

## <span data-ttu-id="9ae5a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9ae5a-104">SYNTAX</span></span>

### <span data-ttu-id="9ae5a-105">ContextParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9ae5a-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ae5a-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ae5a-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ae5a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ae5a-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ae5a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9ae5a-108">DESCRIPTION</span></span>
<span data-ttu-id="9ae5a-109">A **Remove-AzApiManagementCache** parancsmag eltávolítja a gyorsítótárattitást.</span><span class="sxs-lookup"><span data-stu-id="9ae5a-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="9ae5a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9ae5a-110">EXAMPLES</span></span>

### <span data-ttu-id="9ae5a-111">1. példa: A gyorsítótárazási entitás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9ae5a-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="9ae5a-112">Ez a parancsmag eltávolítja a gyorsítótárat `centralus` az Api Management szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="9ae5a-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="9ae5a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ae5a-113">PARAMETERS</span></span>

### <span data-ttu-id="9ae5a-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="9ae5a-114">-CacheId</span></span>
<span data-ttu-id="9ae5a-115">A meglévő cacheId azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9ae5a-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="9ae5a-116">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="9ae5a-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ae5a-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9ae5a-117">-Context</span></span>
<span data-ttu-id="9ae5a-118">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="9ae5a-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9ae5a-119">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="9ae5a-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ae5a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ae5a-120">-DefaultProfile</span></span>
<span data-ttu-id="9ae5a-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ae5a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ae5a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ae5a-122">-InputObject</span></span>
<span data-ttu-id="9ae5a-123">A PsApiManagementCache példánya.</span><span class="sxs-lookup"><span data-stu-id="9ae5a-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="9ae5a-124">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="9ae5a-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ae5a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ae5a-125">-PassThru</span></span>
<span data-ttu-id="9ae5a-126">Ha a megadott érték igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="9ae5a-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="9ae5a-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9ae5a-127">This parameter is optional.</span></span>
<span data-ttu-id="9ae5a-128">Az alapértelmezett érték hamis.</span><span class="sxs-lookup"><span data-stu-id="9ae5a-128">Default value is false.</span></span>

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

### <span data-ttu-id="9ae5a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ae5a-129">-ResourceId</span></span>
<span data-ttu-id="9ae5a-130">Gyorsítótár erőforrásazonosítója arm.</span><span class="sxs-lookup"><span data-stu-id="9ae5a-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="9ae5a-131">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="9ae5a-131">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ae5a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ae5a-132">-Confirm</span></span>
<span data-ttu-id="9ae5a-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9ae5a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ae5a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ae5a-134">-WhatIf</span></span>
<span data-ttu-id="9ae5a-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9ae5a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ae5a-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9ae5a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ae5a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ae5a-137">CommonParameters</span></span>
<span data-ttu-id="9ae5a-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ae5a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ae5a-139">További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ae5a-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ae5a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ae5a-140">INPUTS</span></span>

### <span data-ttu-id="9ae5a-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9ae5a-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9ae5a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9ae5a-142">System.String</span></span>

### <span data-ttu-id="9ae5a-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9ae5a-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9ae5a-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ae5a-144">OUTPUTS</span></span>

### <span data-ttu-id="9ae5a-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9ae5a-145">System.Boolean</span></span>

## <span data-ttu-id="9ae5a-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9ae5a-146">NOTES</span></span>

## <span data-ttu-id="9ae5a-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ae5a-147">RELATED LINKS</span></span>

[<span data-ttu-id="9ae5a-148">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="9ae5a-148">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="9ae5a-149">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="9ae5a-149">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="9ae5a-150">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="9ae5a-150">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
