---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 11a28cb8848c197d9d766b05833e8c0ca3106412
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494697"
---
# <span data-ttu-id="05ccf-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="05ccf-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="05ccf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05ccf-102">SYNOPSIS</span></span>
<span data-ttu-id="05ccf-103">Megkapja a házirend-hozzárendeléseket.</span><span class="sxs-lookup"><span data-stu-id="05ccf-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05ccf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05ccf-104">SYNTAX</span></span>

### <span data-ttu-id="05ccf-105">A lista minden házirend-hozzárendelési paraméterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="05ccf-105">The list all policy assignments parameter set.</span></span> <span data-ttu-id="05ccf-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="05ccf-106">(Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="05ccf-107">A házirend-hozzárendelés neve paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="05ccf-107">The policy assignment name parameter set.</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="05ccf-108">A házirend-hozzárendelés azonosítója paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="05ccf-108">The policy assignment Id parameter set.</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="05ccf-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="05ccf-109">DESCRIPTION</span></span>
<span data-ttu-id="05ccf-110">A **Get-AzureRmPolicyAssignment** parancsmag minden házirend-feladatot vagy adott hozzárendelést beolvas.</span><span class="sxs-lookup"><span data-stu-id="05ccf-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="05ccf-111">A név és a hatókör vagy az azonosító alapján beolvasott házirend-hozzárendelés meghatározása</span><span class="sxs-lookup"><span data-stu-id="05ccf-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="05ccf-112">Példák</span><span class="sxs-lookup"><span data-stu-id="05ccf-112">EXAMPLES</span></span>

### <span data-ttu-id="05ccf-113">1. példa: az összes házirend-hozzárendelés beolvasása</span><span class="sxs-lookup"><span data-stu-id="05ccf-113">Example 1: Get all policy assignments</span></span>
```
PS C:\>Get-AzureRmPolicyAssignment
```

<span data-ttu-id="05ccf-114">Ez a parancs az összes házirend-hozzárendelést megkapja.</span><span class="sxs-lookup"><span data-stu-id="05ccf-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="05ccf-115">2. példa: konkrét házirend-hozzárendelés beszerzése</span><span class="sxs-lookup"><span data-stu-id="05ccf-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="05ccf-116">Az első parancs az Get-AzureRMResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="05ccf-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="05ccf-117">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="05ccf-117">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="05ccf-118">A második parancs beolvassa a PolicyAssignment07 nevű házirend-hozzárendelést annak a hatókörnek a **ResourceId** tulajdonsága, amelyre az $ResourceGroup azonosítja.</span><span class="sxs-lookup"><span data-stu-id="05ccf-118">The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

## <span data-ttu-id="05ccf-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05ccf-119">PARAMETERS</span></span>

### <span data-ttu-id="05ccf-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="05ccf-120">-ApiVersion</span></span>
<span data-ttu-id="05ccf-121">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="05ccf-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="05ccf-122">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="05ccf-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="05ccf-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="05ccf-123">-Id</span></span>
<span data-ttu-id="05ccf-124">Annak a házirend-hozzárendelésnek a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="05ccf-124">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="05ccf-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="05ccf-125">-InformationAction</span></span>
<span data-ttu-id="05ccf-126">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="05ccf-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="05ccf-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="05ccf-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="05ccf-128">Folytassa</span><span class="sxs-lookup"><span data-stu-id="05ccf-128">Continue</span></span>
- <span data-ttu-id="05ccf-129">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="05ccf-129">Ignore</span></span>
- <span data-ttu-id="05ccf-130">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="05ccf-130">Inquire</span></span>
- <span data-ttu-id="05ccf-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="05ccf-131">SilentlyContinue</span></span>
- <span data-ttu-id="05ccf-132">állj</span><span class="sxs-lookup"><span data-stu-id="05ccf-132">Stop</span></span>
- <span data-ttu-id="05ccf-133">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="05ccf-133">Suspend</span></span>

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

### <span data-ttu-id="05ccf-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="05ccf-134">-InformationVariable</span></span>
<span data-ttu-id="05ccf-135">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="05ccf-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="05ccf-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="05ccf-136">-Name</span></span>
<span data-ttu-id="05ccf-137">Annak a házirend-hozzárendelésnek a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="05ccf-137">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05ccf-138">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="05ccf-138">-PolicyDefinitionId</span></span>
<span data-ttu-id="05ccf-139">Annak a házirend-hozzárendelésnek az AZONOSÍTÓját adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="05ccf-139">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set., The policy assignment Id parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05ccf-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="05ccf-140">-Pre</span></span>
<span data-ttu-id="05ccf-141">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="05ccf-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="05ccf-142">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="05ccf-142">-Scope</span></span>
<span data-ttu-id="05ccf-143">Azt a hatókört adja meg, amelynél a program a parancsmagot tartalmazó hozzárendeléshez alkalmazza a házirendet.</span><span class="sxs-lookup"><span data-stu-id="05ccf-143">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="05ccf-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05ccf-144">-DefaultProfile</span></span>
<span data-ttu-id="05ccf-145">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05ccf-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05ccf-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05ccf-146">CommonParameters</span></span>
<span data-ttu-id="05ccf-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05ccf-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05ccf-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05ccf-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05ccf-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05ccf-149">INPUTS</span></span>

## <span data-ttu-id="05ccf-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05ccf-150">OUTPUTS</span></span>

### <span data-ttu-id="05ccf-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="05ccf-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="05ccf-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05ccf-152">NOTES</span></span>

## <span data-ttu-id="05ccf-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05ccf-153">RELATED LINKS</span></span>

[<span data-ttu-id="05ccf-154">Új – AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="05ccf-154">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="05ccf-155">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="05ccf-155">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="05ccf-156">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="05ccf-156">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


