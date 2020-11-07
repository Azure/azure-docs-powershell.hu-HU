---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 2b699219281d64e50694f7e7dd70a965626f7132
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669316"
---
# <span data-ttu-id="767e3-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="767e3-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="767e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="767e3-102">SYNOPSIS</span></span>
<span data-ttu-id="767e3-103">Házirend-hozzárendelés módosítása</span><span class="sxs-lookup"><span data-stu-id="767e3-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="767e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="767e3-104">SYNTAX</span></span>

### <span data-ttu-id="767e3-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="767e3-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="767e3-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="767e3-106">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="767e3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="767e3-107">DESCRIPTION</span></span>
<span data-ttu-id="767e3-108">A **set-AzPolicyAssignment** parancsmag módosította egy házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="767e3-108">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="767e3-109">Adjon meg egy hozzárendelést azonosító alapján vagy név és hatókör szerint.</span><span class="sxs-lookup"><span data-stu-id="767e3-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="767e3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="767e3-110">EXAMPLES</span></span>

### <span data-ttu-id="767e3-111">Példa 1: a megjelenítendő név frissítése</span><span class="sxs-lookup"><span data-stu-id="767e3-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="767e3-112">Az első parancs az Get-AzResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="767e3-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="767e3-113">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="767e3-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="767e3-114">A második parancs az Get-AzPolicyAssignment parancsmag használatával kapja meg a PolicyAssignment nevű házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="767e3-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="767e3-115">A parancs az objektumot a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="767e3-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="767e3-116">A végleges parancs frissíti a megjelenítendő nevet az $ResourceGroup **ResourceId** tulajdonsága által azonosított erőforráscsoport házirend-hozzárendelésében.</span><span class="sxs-lookup"><span data-stu-id="767e3-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="767e3-117">2. példa: felügyelt identitás hozzáadása a házirend-hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="767e3-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="767e3-118">Az első parancs a PolicyAssignment nevű házirend-hozzárendelést az aktuális előfizetésből az Get-AzPolicyAssignment parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="767e3-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="767e3-119">A parancs az objektumot a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="767e3-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="767e3-120">A végleges parancs a felügyelt identitást a házirend-hozzárendeléshez rendeli.</span><span class="sxs-lookup"><span data-stu-id="767e3-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="767e3-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="767e3-121">PARAMETERS</span></span>

### <span data-ttu-id="767e3-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="767e3-122">-ApiVersion</span></span>
<span data-ttu-id="767e3-123">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="767e3-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="767e3-124">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="767e3-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="767e3-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="767e3-125">-AssignIdentity</span></span>
<span data-ttu-id="767e3-126">Azure Active Directory-identitás létrehozása és hozzárendelése ehhez a házirend-hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="767e3-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="767e3-127">Az identitás a "deployIfNotExists" házirendek telepítésének végrehajtásakor lesz használatos.</span><span class="sxs-lookup"><span data-stu-id="767e3-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="767e3-128">Az identitás hozzárendelésekor a hely szükséges.</span><span class="sxs-lookup"><span data-stu-id="767e3-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="767e3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="767e3-129">-DefaultProfile</span></span>
<span data-ttu-id="767e3-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="767e3-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="767e3-131">-Leírás</span><span class="sxs-lookup"><span data-stu-id="767e3-131">-Description</span></span>
<span data-ttu-id="767e3-132">A házirend-hozzárendelés leírása</span><span class="sxs-lookup"><span data-stu-id="767e3-132">The description for policy assignment</span></span>

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

### <span data-ttu-id="767e3-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="767e3-133">-DisplayName</span></span>
<span data-ttu-id="767e3-134">A házirend-hozzárendelés új megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="767e3-134">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="767e3-135">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="767e3-135">-Id</span></span>
<span data-ttu-id="767e3-136">Annak a házirend-hozzárendelésnek a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="767e3-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="767e3-137">-Hely</span><span class="sxs-lookup"><span data-stu-id="767e3-137">-Location</span></span>
<span data-ttu-id="767e3-138">A házirend-hozzárendelés erőforrás-identitásának helye.</span><span class="sxs-lookup"><span data-stu-id="767e3-138">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="767e3-139">Erre akkor van szükség, ha a-AssignIdentity kapcsolót használja.</span><span class="sxs-lookup"><span data-stu-id="767e3-139">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="767e3-140">-Metadata</span><span class="sxs-lookup"><span data-stu-id="767e3-140">-Metadata</span></span>
<span data-ttu-id="767e3-141">A házirend-hozzárendelés frissített metaadatai.</span><span class="sxs-lookup"><span data-stu-id="767e3-141">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="767e3-142">Ez lehet a metaadatokat tartalmazó fájlnév vagy a metaadat karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="767e3-142">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="767e3-143">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="767e3-143">-Name</span></span>
<span data-ttu-id="767e3-144">Annak a házirend-hozzárendelésnek a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="767e3-144">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="767e3-145">-NotScope</span><span class="sxs-lookup"><span data-stu-id="767e3-145">-NotScope</span></span>
<span data-ttu-id="767e3-146">A házirend-hozzárendelés nem hatókörök.</span><span class="sxs-lookup"><span data-stu-id="767e3-146">The policy assignment not scopes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="767e3-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="767e3-147">-Pre</span></span>
<span data-ttu-id="767e3-148">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="767e3-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="767e3-149">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="767e3-149">-Scope</span></span>
<span data-ttu-id="767e3-150">Azt a hatókört adja meg, amelyen a házirendet alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="767e3-150">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="767e3-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="767e3-151">CommonParameters</span></span>
<span data-ttu-id="767e3-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="767e3-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="767e3-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="767e3-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="767e3-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="767e3-154">INPUTS</span></span>

### <span data-ttu-id="767e3-155">System. String</span><span class="sxs-lookup"><span data-stu-id="767e3-155">System.String</span></span>

### <span data-ttu-id="767e3-156">System. string []</span><span class="sxs-lookup"><span data-stu-id="767e3-156">System.String[]</span></span>

## <span data-ttu-id="767e3-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="767e3-157">OUTPUTS</span></span>

### <span data-ttu-id="767e3-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="767e3-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="767e3-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="767e3-159">NOTES</span></span>

## <span data-ttu-id="767e3-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="767e3-160">RELATED LINKS</span></span>

[<span data-ttu-id="767e3-161">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="767e3-161">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="767e3-162">Új – AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="767e3-162">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="767e3-163">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="767e3-163">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


