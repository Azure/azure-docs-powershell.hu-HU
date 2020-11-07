---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: dc54d84886bc9c13fa6a4ecef4e41ef80fa6d4e4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849041"
---
# <span data-ttu-id="299de-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="299de-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="299de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="299de-102">SYNOPSIS</span></span>
<span data-ttu-id="299de-103">Házirend-hozzárendelés módosítása</span><span class="sxs-lookup"><span data-stu-id="299de-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="299de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="299de-104">SYNTAX</span></span>

### <span data-ttu-id="299de-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="299de-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="299de-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="299de-106">IdParameterSet</span></span>
```
Set-AzureRmPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="299de-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="299de-107">DESCRIPTION</span></span>
<span data-ttu-id="299de-108">A **set-AzureRmPolicyAssignment** parancsmag módosította egy házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="299de-108">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="299de-109">Adjon meg egy hozzárendelést azonosító alapján vagy név és hatókör szerint.</span><span class="sxs-lookup"><span data-stu-id="299de-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="299de-110">Példák</span><span class="sxs-lookup"><span data-stu-id="299de-110">EXAMPLES</span></span>

### <span data-ttu-id="299de-111">Példa 1: a megjelenítendő név frissítése</span><span class="sxs-lookup"><span data-stu-id="299de-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="299de-112">Az első parancs az Get-AzureRMResourceGroup parancsmag segítségével a ResourceGroup11 nevű erőforráscsoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="299de-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="299de-113">A parancs az objektumot a $ResourceGroup változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="299de-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="299de-114">A második parancs az Get-AzureRmPolicyAssignment parancsmag használatával kapja meg a PolicyAssignment nevű házirend-feladatot.</span><span class="sxs-lookup"><span data-stu-id="299de-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="299de-115">A parancs az objektumot a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="299de-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="299de-116">A végleges parancs frissíti a megjelenítendő nevet az $ResourceGroup **ResourceId** tulajdonsága által azonosított erőforráscsoport házirend-hozzárendelésében.</span><span class="sxs-lookup"><span data-stu-id="299de-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="299de-117">2. példa: felügyelt identitás hozzáadása a házirend-hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="299de-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="299de-118">Az első parancs a PolicyAssignment nevű házirend-hozzárendelést az aktuális előfizetésből az Get-AzureRmPolicyAssignment parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="299de-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="299de-119">A parancs az objektumot a $PolicyAssignment változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="299de-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="299de-120">A végleges parancs a felügyelt identitást a házirend-hozzárendeléshez rendeli.</span><span class="sxs-lookup"><span data-stu-id="299de-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="299de-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="299de-121">PARAMETERS</span></span>

### <span data-ttu-id="299de-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="299de-122">-ApiVersion</span></span>
<span data-ttu-id="299de-123">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="299de-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="299de-124">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="299de-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="299de-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="299de-125">-AssignIdentity</span></span>
<span data-ttu-id="299de-126">Azure Active Directory-identitás létrehozása és hozzárendelése ehhez a házirend-hozzárendeléshez</span><span class="sxs-lookup"><span data-stu-id="299de-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="299de-127">Az identitás a "deployIfNotExists" házirendek telepítésének végrehajtásakor lesz használatos.</span><span class="sxs-lookup"><span data-stu-id="299de-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="299de-128">Az identitás hozzárendelésekor a hely szükséges.</span><span class="sxs-lookup"><span data-stu-id="299de-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="299de-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="299de-129">-DefaultProfile</span></span>
<span data-ttu-id="299de-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="299de-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="299de-131">-Leírás</span><span class="sxs-lookup"><span data-stu-id="299de-131">-Description</span></span>
<span data-ttu-id="299de-132">A házirend-hozzárendelés leírása</span><span class="sxs-lookup"><span data-stu-id="299de-132">The description for policy assignment</span></span>

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

### <span data-ttu-id="299de-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="299de-133">-DisplayName</span></span>
<span data-ttu-id="299de-134">A házirend-hozzárendelés új megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="299de-134">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="299de-135">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="299de-135">-Id</span></span>
<span data-ttu-id="299de-136">Annak a házirend-hozzárendelésnek a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="299de-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="299de-137">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="299de-137">-InformationAction</span></span>
<span data-ttu-id="299de-138">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="299de-138">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="299de-139">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="299de-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="299de-140">Folytassa</span><span class="sxs-lookup"><span data-stu-id="299de-140">Continue</span></span>
- <span data-ttu-id="299de-141">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="299de-141">Ignore</span></span>
- <span data-ttu-id="299de-142">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="299de-142">Inquire</span></span>
- <span data-ttu-id="299de-143">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="299de-143">SilentlyContinue</span></span>
- <span data-ttu-id="299de-144">állj</span><span class="sxs-lookup"><span data-stu-id="299de-144">Stop</span></span>
- <span data-ttu-id="299de-145">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="299de-145">Suspend</span></span>

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

### <span data-ttu-id="299de-146">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="299de-146">-InformationVariable</span></span>
<span data-ttu-id="299de-147">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="299de-147">Specifies an information variable.</span></span>

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

### <span data-ttu-id="299de-148">-Hely</span><span class="sxs-lookup"><span data-stu-id="299de-148">-Location</span></span>
<span data-ttu-id="299de-149">A házirend-hozzárendelés erőforrás-identitásának helye.</span><span class="sxs-lookup"><span data-stu-id="299de-149">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="299de-150">Erre akkor van szükség, ha a-AssignIdentity kapcsolót használja.</span><span class="sxs-lookup"><span data-stu-id="299de-150">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="299de-151">-Metadata</span><span class="sxs-lookup"><span data-stu-id="299de-151">-Metadata</span></span>
<span data-ttu-id="299de-152">A házirend-hozzárendelés frissített metaadatai.</span><span class="sxs-lookup"><span data-stu-id="299de-152">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="299de-153">Ez lehet a metaadatokat tartalmazó fájlnév vagy a metaadat karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="299de-153">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="299de-154">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="299de-154">-Name</span></span>
<span data-ttu-id="299de-155">Annak a házirend-hozzárendelésnek a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="299de-155">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="299de-156">-NotScope</span><span class="sxs-lookup"><span data-stu-id="299de-156">-NotScope</span></span>
<span data-ttu-id="299de-157">A házirend-hozzárendelés nem hatókörök.</span><span class="sxs-lookup"><span data-stu-id="299de-157">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="299de-158">-Pre</span><span class="sxs-lookup"><span data-stu-id="299de-158">-Pre</span></span>
<span data-ttu-id="299de-159">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="299de-159">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="299de-160">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="299de-160">-Scope</span></span>
<span data-ttu-id="299de-161">Azt a hatókört adja meg, amelyen a házirendet alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="299de-161">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="299de-162">-SKU</span><span class="sxs-lookup"><span data-stu-id="299de-162">-Sku</span></span>
<span data-ttu-id="299de-163">A SKU tulajdonságokat reprezentáló kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="299de-163">A hash table which represents sku properties.</span></span>

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

### <span data-ttu-id="299de-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="299de-164">CommonParameters</span></span>
<span data-ttu-id="299de-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="299de-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="299de-166">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="299de-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="299de-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="299de-167">INPUTS</span></span>

## <span data-ttu-id="299de-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="299de-168">OUTPUTS</span></span>

## <span data-ttu-id="299de-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="299de-169">NOTES</span></span>

## <span data-ttu-id="299de-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="299de-170">RELATED LINKS</span></span>

[<span data-ttu-id="299de-171">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="299de-171">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="299de-172">Új – AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="299de-172">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="299de-173">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="299de-173">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


