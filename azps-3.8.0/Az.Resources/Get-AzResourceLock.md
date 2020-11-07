---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: ea0ee8e46c70e6dd61e352ce0e7bd5da391c0c66
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846177"
---
# <span data-ttu-id="579eb-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="579eb-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="579eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="579eb-102">SYNOPSIS</span></span>
<span data-ttu-id="579eb-103">Erőforrás-zárolást kap.</span><span class="sxs-lookup"><span data-stu-id="579eb-103">Gets a resource lock.</span></span>

## <span data-ttu-id="579eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="579eb-104">SYNTAX</span></span>

### <span data-ttu-id="579eb-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="579eb-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="579eb-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="579eb-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="579eb-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="579eb-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="579eb-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="579eb-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="579eb-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="579eb-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="579eb-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="579eb-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="579eb-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="579eb-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="579eb-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="579eb-112">DESCRIPTION</span></span>
<span data-ttu-id="579eb-113">A **Get-AzResourceLock** parancsmag Azure-erőforrás-zárolásokat kap.</span><span class="sxs-lookup"><span data-stu-id="579eb-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="579eb-114">Példák</span><span class="sxs-lookup"><span data-stu-id="579eb-114">EXAMPLES</span></span>

### <span data-ttu-id="579eb-115">Példa 1: zárolás beszerzése</span><span class="sxs-lookup"><span data-stu-id="579eb-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="579eb-116">Ez a parancs a ContosoSiteLock nevű erőforrás-zárolást kapja meg.</span><span class="sxs-lookup"><span data-stu-id="579eb-116">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="579eb-117">2. példa: az erőforráscsoport vagy a magasabb szintű zárolások lekérése</span><span class="sxs-lookup"><span data-stu-id="579eb-117">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="579eb-118">Ez a parancs beolvassa az erőforrás-zárolásokat az erőforrás csoportban vagy az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="579eb-118">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="579eb-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="579eb-119">PARAMETERS</span></span>

### <span data-ttu-id="579eb-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="579eb-120">-ApiVersion</span></span>
<span data-ttu-id="579eb-121">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="579eb-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="579eb-122">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="579eb-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="579eb-123">-AtScope</span><span class="sxs-lookup"><span data-stu-id="579eb-123">-AtScope</span></span>
<span data-ttu-id="579eb-124">Azt jelzi, hogy ez a parancsmag az összes zárolását visszaadja a megadott hatókörnél vagy fölött.</span><span class="sxs-lookup"><span data-stu-id="579eb-124">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="579eb-125">Ha nem adja meg ezt a paramétert, a parancsmag az összes zárolást visszaadja a hatókör fölött vagy alatt.</span><span class="sxs-lookup"><span data-stu-id="579eb-125">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="579eb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="579eb-126">-DefaultProfile</span></span>
<span data-ttu-id="579eb-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="579eb-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="579eb-128">-LockId</span><span class="sxs-lookup"><span data-stu-id="579eb-128">-LockId</span></span>
<span data-ttu-id="579eb-129">Annak a zárolásnak az AZONOSÍTÓját adja meg, amelyre a parancsmag eljut.</span><span class="sxs-lookup"><span data-stu-id="579eb-129">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="579eb-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="579eb-130">-LockName</span></span>
<span data-ttu-id="579eb-131">Itt adhatja meg annak a zárolásnak a nevét, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="579eb-131">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="579eb-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="579eb-132">-Pre</span></span>
<span data-ttu-id="579eb-133">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="579eb-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="579eb-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="579eb-134">-ResourceGroupName</span></span>
<span data-ttu-id="579eb-135">Annak az erőforráscsoport-csoportnak a neve, amelyhez a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="579eb-135">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="579eb-136">Ez a parancsmag zárolja az erőforráscsoport zárolását.</span><span class="sxs-lookup"><span data-stu-id="579eb-136">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="579eb-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="579eb-137">-ResourceName</span></span>
<span data-ttu-id="579eb-138">Annak az erőforrásnak a nevét adja meg, amelynek a zárolását alkalmazni kívánja.</span><span class="sxs-lookup"><span data-stu-id="579eb-138">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="579eb-139">Ez a parancsmag zárolja ezt az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="579eb-139">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="579eb-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="579eb-140">-ResourceType</span></span>
<span data-ttu-id="579eb-141">Annak az erőforrásnak az erőforrás-típusát adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="579eb-141">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="579eb-142">Ez a parancsmag zárolja ezt az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="579eb-142">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="579eb-143">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="579eb-143">-Scope</span></span>
<span data-ttu-id="579eb-144">Azt a hatókört adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="579eb-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="579eb-145">A parancsmag zárolásokat kap ehhez a hatókörhöz.</span><span class="sxs-lookup"><span data-stu-id="579eb-145">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="579eb-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="579eb-146">-TenantLevel</span></span>
<span data-ttu-id="579eb-147">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="579eb-147">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="579eb-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="579eb-148">CommonParameters</span></span>
<span data-ttu-id="579eb-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="579eb-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="579eb-150">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="579eb-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="579eb-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="579eb-151">INPUTS</span></span>

### <span data-ttu-id="579eb-152">System. String</span><span class="sxs-lookup"><span data-stu-id="579eb-152">System.String</span></span>

## <span data-ttu-id="579eb-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="579eb-153">OUTPUTS</span></span>

### <span data-ttu-id="579eb-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="579eb-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="579eb-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="579eb-155">NOTES</span></span>

## <span data-ttu-id="579eb-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="579eb-156">RELATED LINKS</span></span>

[<span data-ttu-id="579eb-157">Új – AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="579eb-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="579eb-158">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="579eb-158">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="579eb-159">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="579eb-159">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


