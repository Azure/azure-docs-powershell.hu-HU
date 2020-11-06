---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: fcb1283531b35365cc8c07016c839a1152011160
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494695"
---
# <span data-ttu-id="2cd6f-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2cd6f-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="2cd6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2cd6f-102">SYNOPSIS</span></span>
<span data-ttu-id="2cd6f-103">Házirend-hozzárendelés módosítása</span><span class="sxs-lookup"><span data-stu-id="2cd6f-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cd6f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2cd6f-104">SYNTAX</span></span>

### <span data-ttu-id="2cd6f-105">A házirend-hozzárendelés neve paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-105">The policy assignment name parameter set.</span></span> <span data-ttu-id="2cd6f-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="2cd6f-106">(Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2cd6f-107">A házirend-hozzárendelés azonosítója paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-107">The policy assignment Id parameter set.</span></span>
```
Set-AzureRmPolicyAssignment -Id <String> [-DisplayName <String>] [-Description <String>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2cd6f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2cd6f-108">DESCRIPTION</span></span>
<span data-ttu-id="2cd6f-109">A **set-AzureRmPolicyAssignment** parancsmag módosította egy házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-109">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="2cd6f-110">Adjon meg egy hozzárendelést azonosító alapján vagy név és hatókör szerint.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-110">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="2cd6f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2cd6f-111">EXAMPLES</span></span>

### <span data-ttu-id="2cd6f-112">Példa 1: a megjelenítendő név frissítése</span><span class="sxs-lookup"><span data-stu-id="2cd6f-112">Example 1: Update the display name</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment" -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName "Do not allow VM creation"
```

<span data-ttu-id="2cd6f-113">Az első parancs az Get-AzureRMResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-113">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="2cd6f-114">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-114">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="2cd6f-115">A második parancs az Get-AzureRmPolicyAssignment parancsmag használatával kapja meg a PolicyAssignment nevű házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-115">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="2cd6f-116">A parancs az objektumot a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-116">The command stores that object in the $PolicyAssignment variable.</span></span>

<span data-ttu-id="2cd6f-117">A végleges parancs frissíti az $PolicyAssignment **ResourceId** tulajdonsága által azonosított házirend-hozzárendelés megjelenítendő nevét.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-117">The final command updates the display name on the policy assignment identified by the **ResourceId** property of $PolicyAssignment.</span></span>

## <span data-ttu-id="2cd6f-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2cd6f-118">PARAMETERS</span></span>

### <span data-ttu-id="2cd6f-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2cd6f-119">-ApiVersion</span></span>
<span data-ttu-id="2cd6f-120">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2cd6f-121">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="2cd6f-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2cd6f-122">-DisplayName</span></span>
<span data-ttu-id="2cd6f-123">A házirend-hozzárendelés új megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-123">Specifies a new display name for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd6f-124">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="2cd6f-124">-Id</span></span>
<span data-ttu-id="2cd6f-125">Annak a házirend-hozzárendelésnek a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-125">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd6f-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2cd6f-126">-InformationAction</span></span>
<span data-ttu-id="2cd6f-127">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2cd6f-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2cd6f-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2cd6f-129">Folytassa</span><span class="sxs-lookup"><span data-stu-id="2cd6f-129">Continue</span></span>
- <span data-ttu-id="2cd6f-130">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="2cd6f-130">Ignore</span></span>
- <span data-ttu-id="2cd6f-131">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="2cd6f-131">Inquire</span></span>
- <span data-ttu-id="2cd6f-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2cd6f-132">SilentlyContinue</span></span>
- <span data-ttu-id="2cd6f-133">állj</span><span class="sxs-lookup"><span data-stu-id="2cd6f-133">Stop</span></span>
- <span data-ttu-id="2cd6f-134">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="2cd6f-134">Suspend</span></span>

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

### <span data-ttu-id="2cd6f-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2cd6f-135">-InformationVariable</span></span>
<span data-ttu-id="2cd6f-136">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2cd6f-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2cd6f-137">-Name</span></span>
<span data-ttu-id="2cd6f-138">Annak a házirend-hozzárendelésnek a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-138">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd6f-139">-NotScope</span><span class="sxs-lookup"><span data-stu-id="2cd6f-139">-NotScope</span></span>
<span data-ttu-id="2cd6f-140">A házirend-hozzárendelés nem hatókörök.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-140">The policy assignment not scopes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd6f-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="2cd6f-141">-Pre</span></span>
<span data-ttu-id="2cd6f-142">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2cd6f-143">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="2cd6f-143">-Scope</span></span>
<span data-ttu-id="2cd6f-144">Azt a hatókört adja meg, amelyen a házirendet alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-144">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd6f-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cd6f-145">-DefaultProfile</span></span>
<span data-ttu-id="2cd6f-146">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cd6f-147">-Leírás</span><span class="sxs-lookup"><span data-stu-id="2cd6f-147">-Description</span></span>
<span data-ttu-id="2cd6f-148">A házirend-hozzárendelés leírása.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-148">The description for policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd6f-149">-SKU</span><span class="sxs-lookup"><span data-stu-id="2cd6f-149">-Sku</span></span>
<span data-ttu-id="2cd6f-150">A SKU tulajdonságokat reprezentáló kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="2cd6f-150">A hash table which represents sku properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd6f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cd6f-151">CommonParameters</span></span>
<span data-ttu-id="2cd6f-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2cd6f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cd6f-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cd6f-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cd6f-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cd6f-154">INPUTS</span></span>

## <span data-ttu-id="2cd6f-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cd6f-155">OUTPUTS</span></span>

### <span data-ttu-id="2cd6f-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="2cd6f-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2cd6f-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2cd6f-157">NOTES</span></span>

## <span data-ttu-id="2cd6f-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2cd6f-158">RELATED LINKS</span></span>

[<span data-ttu-id="2cd6f-159">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2cd6f-159">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="2cd6f-160">Új – AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2cd6f-160">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="2cd6f-161">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2cd6f-161">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


