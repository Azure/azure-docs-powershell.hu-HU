---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 2dbbb41ce1ad2ee6fc2279e711722090f4f1a6cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165986"
---
# <span data-ttu-id="b597f-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="b597f-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="b597f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b597f-102">SYNOPSIS</span></span>
<span data-ttu-id="b597f-103">Erőforrás-zárolást kap.</span><span class="sxs-lookup"><span data-stu-id="b597f-103">Gets a resource lock.</span></span>

## <span data-ttu-id="b597f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b597f-104">SYNTAX</span></span>

### <span data-ttu-id="b597f-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b597f-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b597f-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="b597f-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b597f-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="b597f-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b597f-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="b597f-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b597f-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="b597f-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b597f-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="b597f-110">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b597f-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b597f-111">DESCRIPTION</span></span>
<span data-ttu-id="b597f-112">A **Get-AzResourceLock** parancsmag lekérte az Azure-erőforrás zárolását.</span><span class="sxs-lookup"><span data-stu-id="b597f-112">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="b597f-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b597f-113">EXAMPLES</span></span>

### <span data-ttu-id="b597f-114">1. példa: Zárolás lekérte</span><span class="sxs-lookup"><span data-stu-id="b597f-114">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="b597f-115">Ez a parancs a ContosoSiteLock nevű erőforrászárolást kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b597f-115">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="b597f-116">2. példa: Zárolások lehozása erőforráscsoport szinten vagy annál magasabb szinten</span><span class="sxs-lookup"><span data-stu-id="b597f-116">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="b597f-117">Ez a parancs az erőforráscsoport vagy az előfizetés erőforrás-zárolását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b597f-117">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="b597f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b597f-118">PARAMETERS</span></span>

### <span data-ttu-id="b597f-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b597f-119">-ApiVersion</span></span>
<span data-ttu-id="b597f-120">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b597f-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b597f-121">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="b597f-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b597f-122">-AtScope</span><span class="sxs-lookup"><span data-stu-id="b597f-122">-AtScope</span></span>
<span data-ttu-id="b597f-123">Azt jelzi, hogy ez a parancsmag a megadott hatókörön belül vagy fölötti összes zárolást visszaadja.</span><span class="sxs-lookup"><span data-stu-id="b597f-123">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="b597f-124">Ha nem adja meg ezt a paramétert, a parancsmag az összes zárolást visszaadja a hatókör felett vagy alatt.</span><span class="sxs-lookup"><span data-stu-id="b597f-124">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b597f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b597f-125">-DefaultProfile</span></span>
<span data-ttu-id="b597f-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b597f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b597f-127">-LockId</span><span class="sxs-lookup"><span data-stu-id="b597f-127">-LockId</span></span>
<span data-ttu-id="b597f-128">A parancsmag által lekért zárolás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b597f-128">Specifies the ID of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b597f-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="b597f-129">-LockName</span></span>
<span data-ttu-id="b597f-130">A parancsmag által lekért lakat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b597f-130">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b597f-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="b597f-131">-Pre</span></span>
<span data-ttu-id="b597f-132">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="b597f-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b597f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b597f-133">-ResourceGroupName</span></span>
<span data-ttu-id="b597f-134">Annak az erőforráscsoportnak a nevét adja meg, amelyre a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="b597f-134">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="b597f-135">Ez a parancsmag zárolja az erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="b597f-135">This cmdlet gets locks for this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b597f-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b597f-136">-ResourceName</span></span>
<span data-ttu-id="b597f-137">Annak az erőforrásnak a nevét adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="b597f-137">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="b597f-138">Ez a parancsmag zárolja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="b597f-138">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b597f-139">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b597f-139">-ResourceType</span></span>
<span data-ttu-id="b597f-140">Annak az erőforrásnak az erőforrástípusát adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="b597f-140">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="b597f-141">Ez a parancsmag zárolja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="b597f-141">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b597f-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="b597f-142">-Scope</span></span>
<span data-ttu-id="b597f-143">A zárolás hatókörét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b597f-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="b597f-144">A parancsmag zárolást kap ehhez a hatókörhez.</span><span class="sxs-lookup"><span data-stu-id="b597f-144">The cmdlet gets locks for this scope.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b597f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b597f-145">CommonParameters</span></span>
<span data-ttu-id="b597f-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b597f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b597f-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b597f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b597f-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b597f-148">INPUTS</span></span>

### <span data-ttu-id="b597f-149">System.String</span><span class="sxs-lookup"><span data-stu-id="b597f-149">System.String</span></span>

## <span data-ttu-id="b597f-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b597f-150">OUTPUTS</span></span>

### <span data-ttu-id="b597f-151">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="b597f-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b597f-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b597f-152">NOTES</span></span>

## <span data-ttu-id="b597f-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b597f-153">RELATED LINKS</span></span>

[<span data-ttu-id="b597f-154">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="b597f-154">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="b597f-155">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="b597f-155">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="b597f-156">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="b597f-156">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


