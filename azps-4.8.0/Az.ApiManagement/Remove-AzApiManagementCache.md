---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: ffca6c1bc32d809f7bbb93c3b76dd9490f9fafb8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025580"
---
# <span data-ttu-id="a3ede-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a3ede-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="a3ede-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3ede-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ede-103">Eltávolítja a gyorsítótár entitást.</span><span class="sxs-lookup"><span data-stu-id="a3ede-103">Removes the cache entity.</span></span>

## <span data-ttu-id="a3ede-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3ede-104">SYNTAX</span></span>

### <span data-ttu-id="a3ede-105">ContextParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a3ede-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3ede-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3ede-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3ede-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3ede-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3ede-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3ede-108">DESCRIPTION</span></span>
<span data-ttu-id="a3ede-109">A parancsmag **eltávolítása – AzApiManagementCache** eltávolítja a gyorsítótár entitást.</span><span class="sxs-lookup"><span data-stu-id="a3ede-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="a3ede-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a3ede-110">EXAMPLES</span></span>

### <span data-ttu-id="a3ede-111">1. példa: a gyorsítótár-entitás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a3ede-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="a3ede-112">Ez a parancsmag eltávolítja a gyorsítótárat az `centralus` API-kezelési szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="a3ede-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="a3ede-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3ede-113">PARAMETERS</span></span>

### <span data-ttu-id="a3ede-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="a3ede-114">-CacheId</span></span>
<span data-ttu-id="a3ede-115">A meglévő cacheId azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a3ede-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="a3ede-116">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="a3ede-116">This parameter is required.</span></span>

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

### <span data-ttu-id="a3ede-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a3ede-117">-Context</span></span>
<span data-ttu-id="a3ede-118">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="a3ede-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a3ede-119">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="a3ede-119">This parameter is required.</span></span>

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

### <span data-ttu-id="a3ede-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ede-120">-DefaultProfile</span></span>
<span data-ttu-id="a3ede-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3ede-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3ede-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3ede-122">-InputObject</span></span>
<span data-ttu-id="a3ede-123">A PsApiManagementCache példánya.</span><span class="sxs-lookup"><span data-stu-id="a3ede-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="a3ede-124">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="a3ede-124">This parameter is required.</span></span>

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

### <span data-ttu-id="a3ede-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3ede-125">-PassThru</span></span>
<span data-ttu-id="a3ede-126">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="a3ede-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="a3ede-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="a3ede-127">This parameter is optional.</span></span>
<span data-ttu-id="a3ede-128">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="a3ede-128">Default value is false.</span></span>

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

### <span data-ttu-id="a3ede-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3ede-129">-ResourceId</span></span>
<span data-ttu-id="a3ede-130">A kar ResourceId a gyorsítótárból.</span><span class="sxs-lookup"><span data-stu-id="a3ede-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="a3ede-131">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="a3ede-131">This parameter is required.</span></span>

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

### <span data-ttu-id="a3ede-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a3ede-132">-Confirm</span></span>
<span data-ttu-id="a3ede-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a3ede-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3ede-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3ede-134">-WhatIf</span></span>
<span data-ttu-id="a3ede-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a3ede-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3ede-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a3ede-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3ede-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ede-137">CommonParameters</span></span>
<span data-ttu-id="a3ede-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3ede-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ede-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a3ede-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ede-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3ede-140">INPUTS</span></span>

### <span data-ttu-id="a3ede-141">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a3ede-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a3ede-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a3ede-142">System.String</span></span>

### <span data-ttu-id="a3ede-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a3ede-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a3ede-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3ede-144">OUTPUTS</span></span>

### <span data-ttu-id="a3ede-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3ede-145">System.Boolean</span></span>

## <span data-ttu-id="a3ede-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3ede-146">NOTES</span></span>

## <span data-ttu-id="a3ede-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3ede-147">RELATED LINKS</span></span>

[<span data-ttu-id="a3ede-148">Új – AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a3ede-148">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="a3ede-149">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a3ede-149">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="a3ede-150">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a3ede-150">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
