---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 2dbbb41ce1ad2ee6fc2279e711722090f4f1a6cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182174"
---
# <span data-ttu-id="12cf9-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="12cf9-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="12cf9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="12cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="12cf9-103">Erőforrás-zárolást kap.</span><span class="sxs-lookup"><span data-stu-id="12cf9-103">Gets a resource lock.</span></span>

## <span data-ttu-id="12cf9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="12cf9-104">SYNTAX</span></span>

### <span data-ttu-id="12cf9-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="12cf9-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12cf9-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="12cf9-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12cf9-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="12cf9-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12cf9-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="12cf9-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12cf9-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="12cf9-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12cf9-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="12cf9-110">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12cf9-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="12cf9-111">DESCRIPTION</span></span>
<span data-ttu-id="12cf9-112">A **Get-AzResourceLock** parancsmag Azure-erőforrás-zárolásokat kap.</span><span class="sxs-lookup"><span data-stu-id="12cf9-112">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="12cf9-113">Példák</span><span class="sxs-lookup"><span data-stu-id="12cf9-113">EXAMPLES</span></span>

### <span data-ttu-id="12cf9-114">Példa 1: zárolás beszerzése</span><span class="sxs-lookup"><span data-stu-id="12cf9-114">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="12cf9-115">Ez a parancs a ContosoSiteLock nevű erőforrás-zárolást kapja meg.</span><span class="sxs-lookup"><span data-stu-id="12cf9-115">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="12cf9-116">2. példa: az erőforráscsoport vagy a magasabb szintű zárolások lekérése</span><span class="sxs-lookup"><span data-stu-id="12cf9-116">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="12cf9-117">Ez a parancs beolvassa az erőforrás-zárolásokat az erőforrás csoportban vagy az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="12cf9-117">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="12cf9-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="12cf9-118">PARAMETERS</span></span>

### <span data-ttu-id="12cf9-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="12cf9-119">-ApiVersion</span></span>
<span data-ttu-id="12cf9-120">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="12cf9-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="12cf9-121">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="12cf9-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="12cf9-122">-AtScope</span><span class="sxs-lookup"><span data-stu-id="12cf9-122">-AtScope</span></span>
<span data-ttu-id="12cf9-123">Azt jelzi, hogy ez a parancsmag az összes zárolását visszaadja a megadott hatókörnél vagy fölött.</span><span class="sxs-lookup"><span data-stu-id="12cf9-123">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="12cf9-124">Ha nem adja meg ezt a paramétert, a parancsmag az összes zárolást visszaadja a hatókör fölött vagy alatt.</span><span class="sxs-lookup"><span data-stu-id="12cf9-124">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="12cf9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12cf9-125">-DefaultProfile</span></span>
<span data-ttu-id="12cf9-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="12cf9-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12cf9-127">-LockId</span><span class="sxs-lookup"><span data-stu-id="12cf9-127">-LockId</span></span>
<span data-ttu-id="12cf9-128">Annak a zárolásnak az AZONOSÍTÓját adja meg, amelyre a parancsmag eljut.</span><span class="sxs-lookup"><span data-stu-id="12cf9-128">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="12cf9-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="12cf9-129">-LockName</span></span>
<span data-ttu-id="12cf9-130">Itt adhatja meg annak a zárolásnak a nevét, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="12cf9-130">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="12cf9-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="12cf9-131">-Pre</span></span>
<span data-ttu-id="12cf9-132">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="12cf9-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="12cf9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12cf9-133">-ResourceGroupName</span></span>
<span data-ttu-id="12cf9-134">Annak az erőforráscsoport-csoportnak a neve, amelyhez a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="12cf9-134">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="12cf9-135">Ez a parancsmag zárolja az erőforráscsoport zárolását.</span><span class="sxs-lookup"><span data-stu-id="12cf9-135">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="12cf9-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="12cf9-136">-ResourceName</span></span>
<span data-ttu-id="12cf9-137">Annak az erőforrásnak a nevét adja meg, amelynek a zárolását alkalmazni kívánja.</span><span class="sxs-lookup"><span data-stu-id="12cf9-137">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="12cf9-138">Ez a parancsmag zárolja ezt az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="12cf9-138">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="12cf9-139">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="12cf9-139">-ResourceType</span></span>
<span data-ttu-id="12cf9-140">Annak az erőforrásnak az erőforrás-típusát adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="12cf9-140">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="12cf9-141">Ez a parancsmag zárolja ezt az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="12cf9-141">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="12cf9-142">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="12cf9-142">-Scope</span></span>
<span data-ttu-id="12cf9-143">Azt a hatókört adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="12cf9-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="12cf9-144">A parancsmag zárolásokat kap ehhez a hatókörhöz.</span><span class="sxs-lookup"><span data-stu-id="12cf9-144">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="12cf9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12cf9-145">CommonParameters</span></span>
<span data-ttu-id="12cf9-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="12cf9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12cf9-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="12cf9-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12cf9-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="12cf9-148">INPUTS</span></span>

### <span data-ttu-id="12cf9-149">System. String</span><span class="sxs-lookup"><span data-stu-id="12cf9-149">System.String</span></span>

## <span data-ttu-id="12cf9-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12cf9-150">OUTPUTS</span></span>

### <span data-ttu-id="12cf9-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="12cf9-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="12cf9-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="12cf9-152">NOTES</span></span>

## <span data-ttu-id="12cf9-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12cf9-153">RELATED LINKS</span></span>

[<span data-ttu-id="12cf9-154">Új – AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="12cf9-154">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="12cf9-155">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="12cf9-155">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="12cf9-156">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="12cf9-156">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


