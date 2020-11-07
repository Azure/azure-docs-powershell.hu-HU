---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: 81e7ab170dc43af0cf712fd9be3e831f33f7fd97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849489"
---
# <span data-ttu-id="cddc0-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="cddc0-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="cddc0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cddc0-102">SYNOPSIS</span></span>
<span data-ttu-id="cddc0-103">Erőforrás-zárolást kap.</span><span class="sxs-lookup"><span data-stu-id="cddc0-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cddc0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cddc0-104">SYNTAX</span></span>

### <span data-ttu-id="cddc0-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cddc0-105">ByResourceGroup</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cddc0-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="cddc0-106">ByResourceGroupLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cddc0-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="cddc0-107">BySpecifiedScope</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cddc0-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="cddc0-108">BySubscription</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cddc0-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="cddc0-109">BySubscriptionLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cddc0-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="cddc0-110">ByTenantLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cddc0-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="cddc0-111">ByLockId</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cddc0-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="cddc0-112">DESCRIPTION</span></span>
<span data-ttu-id="cddc0-113">A **Get-AzureRmResourceLock** parancsmag Azure-erőforrás-zárolásokat kap.</span><span class="sxs-lookup"><span data-stu-id="cddc0-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="cddc0-114">Példák</span><span class="sxs-lookup"><span data-stu-id="cddc0-114">EXAMPLES</span></span>

### <span data-ttu-id="cddc0-115">Példa 1: zárolás beszerzése</span><span class="sxs-lookup"><span data-stu-id="cddc0-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="cddc0-116">Ez a parancs a ContosoSiteLock nevű erőforrás-zárolást kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cddc0-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="cddc0-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cddc0-117">PARAMETERS</span></span>

### <span data-ttu-id="cddc0-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cddc0-118">-ApiVersion</span></span>
<span data-ttu-id="cddc0-119">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cddc0-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="cddc0-120">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="cddc0-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="cddc0-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="cddc0-121">-AtScope</span></span>
<span data-ttu-id="cddc0-122">Azt jelzi, hogy ez a parancsmag az összes zárolását visszaadja a megadott hatókörnél vagy fölött.</span><span class="sxs-lookup"><span data-stu-id="cddc0-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="cddc0-123">Ha nem adja meg ezt a paramétert, a parancsmag az összes zárolást visszaadja a hatókör fölött vagy alatt.</span><span class="sxs-lookup"><span data-stu-id="cddc0-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="cddc0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cddc0-124">-DefaultProfile</span></span>
<span data-ttu-id="cddc0-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cddc0-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cddc0-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="cddc0-126">-InformationAction</span></span>
<span data-ttu-id="cddc0-127">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="cddc0-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="cddc0-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="cddc0-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cddc0-129">Folytassa</span><span class="sxs-lookup"><span data-stu-id="cddc0-129">Continue</span></span>
- <span data-ttu-id="cddc0-130">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="cddc0-130">Ignore</span></span>
- <span data-ttu-id="cddc0-131">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="cddc0-131">Inquire</span></span>
- <span data-ttu-id="cddc0-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cddc0-132">SilentlyContinue</span></span>
- <span data-ttu-id="cddc0-133">állj</span><span class="sxs-lookup"><span data-stu-id="cddc0-133">Stop</span></span>
- <span data-ttu-id="cddc0-134">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="cddc0-134">Suspend</span></span>

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

### <span data-ttu-id="cddc0-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cddc0-135">-InformationVariable</span></span>
<span data-ttu-id="cddc0-136">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="cddc0-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cddc0-137">-LockId</span><span class="sxs-lookup"><span data-stu-id="cddc0-137">-LockId</span></span>
<span data-ttu-id="cddc0-138">Annak a zárolásnak az AZONOSÍTÓját adja meg, amelyre a parancsmag eljut.</span><span class="sxs-lookup"><span data-stu-id="cddc0-138">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cddc0-139">-LockName</span><span class="sxs-lookup"><span data-stu-id="cddc0-139">-LockName</span></span>
<span data-ttu-id="cddc0-140">Itt adhatja meg annak a zárolásnak a nevét, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="cddc0-140">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cddc0-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="cddc0-141">-Pre</span></span>
<span data-ttu-id="cddc0-142">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="cddc0-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="cddc0-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cddc0-143">-ResourceGroupName</span></span>
<span data-ttu-id="cddc0-144">Annak az erőforráscsoport-csoportnak a neve, amelyhez a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="cddc0-144">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="cddc0-145">Ez a parancsmag zárolja az erőforráscsoport zárolását.</span><span class="sxs-lookup"><span data-stu-id="cddc0-145">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="cddc0-146">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="cddc0-146">-ResourceName</span></span>
<span data-ttu-id="cddc0-147">Annak az erőforrásnak a nevét adja meg, amelynek a zárolását alkalmazni kívánja.</span><span class="sxs-lookup"><span data-stu-id="cddc0-147">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="cddc0-148">Ez a parancsmag zárolja ezt az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="cddc0-148">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="cddc0-149">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="cddc0-149">-ResourceType</span></span>
<span data-ttu-id="cddc0-150">Annak az erőforrásnak az erőforrás-típusát adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="cddc0-150">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="cddc0-151">Ez a parancsmag zárolja ezt az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="cddc0-151">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="cddc0-152">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="cddc0-152">-Scope</span></span>
<span data-ttu-id="cddc0-153">Azt a hatókört adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="cddc0-153">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="cddc0-154">A parancsmag zárolásokat kap ehhez a hatókörhöz.</span><span class="sxs-lookup"><span data-stu-id="cddc0-154">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="cddc0-155">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="cddc0-155">-TenantLevel</span></span>
<span data-ttu-id="cddc0-156">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="cddc0-156">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="cddc0-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cddc0-157">CommonParameters</span></span>
<span data-ttu-id="cddc0-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cddc0-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cddc0-159">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cddc0-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cddc0-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cddc0-160">INPUTS</span></span>

## <span data-ttu-id="cddc0-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cddc0-161">OUTPUTS</span></span>

## <span data-ttu-id="cddc0-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cddc0-162">NOTES</span></span>

## <span data-ttu-id="cddc0-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cddc0-163">RELATED LINKS</span></span>

[<span data-ttu-id="cddc0-164">Új – AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="cddc0-164">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="cddc0-165">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="cddc0-165">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="cddc0-166">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="cddc0-166">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


