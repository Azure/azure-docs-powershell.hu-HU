---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: e774b333703714246de852d3f72ba704d7122b98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843406"
---
# <span data-ttu-id="f0c1e-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f0c1e-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="f0c1e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f0c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c1e-103">Erőforrás-zárolást kap.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-103">Gets a resource lock.</span></span>

## <span data-ttu-id="f0c1e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f0c1e-104">SYNTAX</span></span>

### <span data-ttu-id="f0c1e-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f0c1e-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f0c1e-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="f0c1e-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f0c1e-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="f0c1e-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f0c1e-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="f0c1e-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f0c1e-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="f0c1e-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f0c1e-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="f0c1e-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f0c1e-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="f0c1e-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f0c1e-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="f0c1e-112">DESCRIPTION</span></span>
<span data-ttu-id="f0c1e-113">A **Get-AzResourceLock** parancsmag Azure-erőforrás-zárolásokat kap.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="f0c1e-114">Példák</span><span class="sxs-lookup"><span data-stu-id="f0c1e-114">EXAMPLES</span></span>

### <span data-ttu-id="f0c1e-115">Példa 1: zárolás beszerzése</span><span class="sxs-lookup"><span data-stu-id="f0c1e-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f0c1e-116">Ez a parancs a ContosoSiteLock nevű erőforrás-zárolást kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="f0c1e-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f0c1e-117">PARAMETERS</span></span>

### <span data-ttu-id="f0c1e-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f0c1e-118">-ApiVersion</span></span>
<span data-ttu-id="f0c1e-119">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f0c1e-120">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f0c1e-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="f0c1e-121">-AtScope</span></span>
<span data-ttu-id="f0c1e-122">Azt jelzi, hogy ez a parancsmag az összes zárolását visszaadja a megadott hatókörnél vagy fölött.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="f0c1e-123">Ha nem adja meg ezt a paramétert, a parancsmag az összes zárolást visszaadja a hatókör fölött vagy alatt.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="f0c1e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c1e-124">-DefaultProfile</span></span>
<span data-ttu-id="f0c1e-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f0c1e-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c1e-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f0c1e-126">-InformationAction</span></span>
<span data-ttu-id="f0c1e-127">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="f0c1e-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f0c1e-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f0c1e-129">Folytassa</span><span class="sxs-lookup"><span data-stu-id="f0c1e-129">Continue</span></span>
- <span data-ttu-id="f0c1e-130">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="f0c1e-130">Ignore</span></span>
- <span data-ttu-id="f0c1e-131">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="f0c1e-131">Inquire</span></span>
- <span data-ttu-id="f0c1e-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f0c1e-132">SilentlyContinue</span></span>
- <span data-ttu-id="f0c1e-133">állj</span><span class="sxs-lookup"><span data-stu-id="f0c1e-133">Stop</span></span>
- <span data-ttu-id="f0c1e-134">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="f0c1e-134">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c1e-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f0c1e-135">-InformationVariable</span></span>
<span data-ttu-id="f0c1e-136">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-136">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c1e-137">-LockId</span><span class="sxs-lookup"><span data-stu-id="f0c1e-137">-LockId</span></span>
<span data-ttu-id="f0c1e-138">Annak a zárolásnak az AZONOSÍTÓját adja meg, amelyre a parancsmag eljut.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-138">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f0c1e-139">-LockName</span><span class="sxs-lookup"><span data-stu-id="f0c1e-139">-LockName</span></span>
<span data-ttu-id="f0c1e-140">Itt adhatja meg annak a zárolásnak a nevét, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-140">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f0c1e-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="f0c1e-141">-Pre</span></span>
<span data-ttu-id="f0c1e-142">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f0c1e-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0c1e-143">-ResourceGroupName</span></span>
<span data-ttu-id="f0c1e-144">Annak az erőforráscsoport-csoportnak a neve, amelyhez a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-144">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="f0c1e-145">Ez a parancsmag zárolja az erőforráscsoport zárolását.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-145">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="f0c1e-146">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f0c1e-146">-ResourceName</span></span>
<span data-ttu-id="f0c1e-147">Annak az erőforrásnak a nevét adja meg, amelynek a zárolását alkalmazni kívánja.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-147">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="f0c1e-148">Ez a parancsmag zárolja ezt az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-148">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="f0c1e-149">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f0c1e-149">-ResourceType</span></span>
<span data-ttu-id="f0c1e-150">Annak az erőforrásnak az erőforrás-típusát adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-150">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="f0c1e-151">Ez a parancsmag zárolja ezt az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-151">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="f0c1e-152">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="f0c1e-152">-Scope</span></span>
<span data-ttu-id="f0c1e-153">Azt a hatókört adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-153">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="f0c1e-154">A parancsmag zárolásokat kap ehhez a hatókörhöz.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-154">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="f0c1e-155">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="f0c1e-155">-TenantLevel</span></span>
<span data-ttu-id="f0c1e-156">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="f0c1e-156">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="f0c1e-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c1e-157">CommonParameters</span></span>
<span data-ttu-id="f0c1e-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f0c1e-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c1e-159">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0c1e-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c1e-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0c1e-160">INPUTS</span></span>

## <span data-ttu-id="f0c1e-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0c1e-161">OUTPUTS</span></span>

## <span data-ttu-id="f0c1e-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f0c1e-162">NOTES</span></span>

## <span data-ttu-id="f0c1e-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0c1e-163">RELATED LINKS</span></span>

[<span data-ttu-id="f0c1e-164">Új – AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f0c1e-164">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="f0c1e-165">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f0c1e-165">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="f0c1e-166">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f0c1e-166">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


