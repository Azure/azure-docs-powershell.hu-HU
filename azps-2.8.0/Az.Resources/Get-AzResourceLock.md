---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 7c9a9da46da232e6b8a7e81e9b698d2b76513c71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838934"
---
# <span data-ttu-id="b5cd6-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="b5cd6-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="b5cd6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="b5cd6-103">Erőforrás-zárolást kap.</span><span class="sxs-lookup"><span data-stu-id="b5cd6-103">Gets a resource lock.</span></span>

## <span data-ttu-id="b5cd6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5cd6-104">SYNTAX</span></span>

### <span data-ttu-id="b5cd6-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b5cd6-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5cd6-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="b5cd6-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5cd6-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="b5cd6-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5cd6-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="b5cd6-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5cd6-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="b5cd6-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5cd6-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="b5cd6-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5cd6-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="b5cd6-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5cd6-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5cd6-112">DESCRIPTION</span></span>
<span data-ttu-id="b5cd6-113">A **Get-AzResourceLock** parancsmag Azure-erőforrás-zárolásokat kap.</span><span class="sxs-lookup"><span data-stu-id="b5cd6-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="b5cd6-114">Példák</span><span class="sxs-lookup"><span data-stu-id="b5cd6-114">EXAMPLES</span></span>

### <span data-ttu-id="b5cd6-115">Példa 1: zárolás beszerzése</span><span class="sxs-lookup"><span data-stu-id="b5cd6-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="b5cd6-116">Ez a parancs a ContosoSiteLock nevű erőforrás-zárolást kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b5cd6-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="b5cd6-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5cd6-117">PARAMETERS</span></span>

### <span data-ttu-id="b5cd6-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b5cd6-118">-ApiVersion</span></span>
<span data-ttu-id="b5cd6-119">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5cd6-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b5cd6-120">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="b5cd6-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b5cd6-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="b5cd6-121">-AtScope</span></span>
<span data-ttu-id="b5cd6-122">Azt jelzi, hogy ez a parancsmag az összes zárolását visszaadja a megadott hatókörnél vagy fölött.</span><span class="sxs-lookup"><span data-stu-id="b5cd6-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="b5cd6-123">Ha nem adja meg ezt a paramétert, a parancsmag az összes zárolást visszaadja a hatókör fölött vagy alatt.</span><span class="sxs-lookup"><span data-stu-id="b5cd6-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="b5cd6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5cd6-124">-DefaultProfile</span></span>
<span data-ttu-id="b5cd6-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b5cd6-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5cd6-126">-LockId</span><span class="sxs-lookup"><span data-stu-id="b5cd6-126">-LockId</span></span>
<span data-ttu-id="b5cd6-127">Annak a zárolásnak az AZONOSÍTÓját adja meg, amelyre a parancsmag eljut.</span><span class="sxs-lookup"><span data-stu-id="b5cd6-127">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b5cd6-128">-LockName</span><span class="sxs-lookup"><span data-stu-id="b5cd6-128">-LockName</span></span>
<span data-ttu-id="b5cd6-129">Itt adhatja meg annak a zárolásnak a nevét, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="b5cd6-129">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b5cd6-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="b5cd6-130">-Pre</span></span>
<span data-ttu-id="b5cd6-131">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="b5cd6-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b5cd6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5cd6-132">-ResourceGroupName</span></span>
<span data-ttu-id="b5cd6-133">Annak az erőforráscsoport-csoportnak a neve, amelyhez a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="b5cd6-133">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="b5cd6-134">Ez a parancsmag zárolja az erőforráscsoport zárolását.</span><span class="sxs-lookup"><span data-stu-id="b5cd6-134">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="b5cd6-135">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b5cd6-135">-ResourceName</span></span>
<span data-ttu-id="b5cd6-136">Annak az erőforrásnak a nevét adja meg, amelynek a zárolását alkalmazni kívánja.</span><span class="sxs-lookup"><span data-stu-id="b5cd6-136">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="b5cd6-137">Ez a parancsmag zárolja ezt az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="b5cd6-137">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="b5cd6-138">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b5cd6-138">-ResourceType</span></span>
<span data-ttu-id="b5cd6-139">Annak az erőforrásnak az erőforrás-típusát adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="b5cd6-139">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="b5cd6-140">Ez a parancsmag zárolja ezt az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="b5cd6-140">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="b5cd6-141">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="b5cd6-141">-Scope</span></span>
<span data-ttu-id="b5cd6-142">Azt a hatókört adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="b5cd6-142">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="b5cd6-143">A parancsmag zárolásokat kap ehhez a hatókörhöz.</span><span class="sxs-lookup"><span data-stu-id="b5cd6-143">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="b5cd6-144">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="b5cd6-144">-TenantLevel</span></span>
<span data-ttu-id="b5cd6-145">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="b5cd6-145">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="b5cd6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5cd6-146">CommonParameters</span></span>
<span data-ttu-id="b5cd6-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5cd6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5cd6-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5cd6-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5cd6-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5cd6-149">INPUTS</span></span>

### <span data-ttu-id="b5cd6-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b5cd6-150">System.String</span></span>

## <span data-ttu-id="b5cd6-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5cd6-151">OUTPUTS</span></span>

### <span data-ttu-id="b5cd6-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b5cd6-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b5cd6-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5cd6-153">NOTES</span></span>

## <span data-ttu-id="b5cd6-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5cd6-154">RELATED LINKS</span></span>

[<span data-ttu-id="b5cd6-155">Új – AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="b5cd6-155">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="b5cd6-156">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="b5cd6-156">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="b5cd6-157">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="b5cd6-157">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


