---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: 2404c0f2dc6c357503f23e7ed509f1c58c352c8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679946"
---
# <span data-ttu-id="a4480-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a4480-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="a4480-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4480-102">SYNOPSIS</span></span>
<span data-ttu-id="a4480-103">Módosította a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="a4480-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4480-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4480-104">SYNTAX</span></span>

### <span data-ttu-id="a4480-105">A Policy definition Name paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="a4480-105">The policy definition name parameter set.</span></span> <span data-ttu-id="a4480-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="a4480-106">(Default)</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a4480-107">A házirend-definíciós azonosító paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="a4480-107">The policy definition Id parameter set.</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a4480-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4480-108">DESCRIPTION</span></span>
<span data-ttu-id="a4480-109">A **set-AzureRmPolicyDefinition** parancsmag módosította a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="a4480-109">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="a4480-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a4480-110">EXAMPLES</span></span>

### <span data-ttu-id="a4480-111">Példa 1: házirend-definíció leírásának frissítése</span><span class="sxs-lookup"><span data-stu-id="a4480-111">Example 1: Update the description of a policy definition</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
PS C:\> Set-AzureRmPolicyDefinition -Id $Policy.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="a4480-112">Az első parancs az Get-AzureRmPolicyDefinition parancsmag használatával megkapja a VMPolicyDefinition nevű házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="a4480-112">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="a4480-113">A parancs az objektumot a $PolicyDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a4480-113">The command stores that object in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="a4480-114">A második parancs frissíti a $PolicyDefinition **ResourceId** tulajdonsága által azonosított házirend-definíció leírását.</span><span class="sxs-lookup"><span data-stu-id="a4480-114">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="a4480-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4480-115">PARAMETERS</span></span>

### <span data-ttu-id="a4480-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a4480-116">-ApiVersion</span></span>
<span data-ttu-id="a4480-117">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4480-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a4480-118">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="a4480-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a4480-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="a4480-119">-Description</span></span>
<span data-ttu-id="a4480-120">A házirend-definíció új leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4480-120">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="a4480-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a4480-121">-DisplayName</span></span>
<span data-ttu-id="a4480-122">A házirend-definíció új megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4480-122">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="a4480-123">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="a4480-123">-Id</span></span>
<span data-ttu-id="a4480-124">Annak a házirend-definíciónak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="a4480-124">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4480-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a4480-125">-InformationAction</span></span>
<span data-ttu-id="a4480-126">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="a4480-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a4480-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a4480-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a4480-128">Folytassa</span><span class="sxs-lookup"><span data-stu-id="a4480-128">Continue</span></span>
- <span data-ttu-id="a4480-129">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="a4480-129">Ignore</span></span>
- <span data-ttu-id="a4480-130">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="a4480-130">Inquire</span></span>
- <span data-ttu-id="a4480-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a4480-131">SilentlyContinue</span></span>
- <span data-ttu-id="a4480-132">állj</span><span class="sxs-lookup"><span data-stu-id="a4480-132">Stop</span></span>
- <span data-ttu-id="a4480-133">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="a4480-133">Suspend</span></span>

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

### <span data-ttu-id="a4480-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a4480-134">-InformationVariable</span></span>
<span data-ttu-id="a4480-135">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="a4480-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a4480-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a4480-136">-Name</span></span>
<span data-ttu-id="a4480-137">Annak a házirend-definíciónak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="a4480-137">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4480-138">-Házirend</span><span class="sxs-lookup"><span data-stu-id="a4480-138">-Policy</span></span>
<span data-ttu-id="a4480-139">A házirend-definíció új házirend-szabályát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4480-139">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="a4480-140">Megadhatja a. JSON fájlok elérési útját, vagy a házirendet a JavaScript-objektum formátumban (JSON) tartalmazó karakterláncban.</span><span class="sxs-lookup"><span data-stu-id="a4480-140">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="a4480-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="a4480-141">-Pre</span></span>
<span data-ttu-id="a4480-142">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="a4480-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a4480-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4480-143">-DefaultProfile</span></span>
<span data-ttu-id="a4480-144">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4480-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4480-145">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a4480-145">-Metadata</span></span>
<span data-ttu-id="a4480-146">A házirend-definíció metaadatai.</span><span class="sxs-lookup"><span data-stu-id="a4480-146">The metadata for policy definition.</span></span> <span data-ttu-id="a4480-147">Ez lehet a metaadatokat tartalmazó fájlnév vagy a metaadatok karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="a4480-147">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="a4480-148">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="a4480-148">-Parameter</span></span>
<span data-ttu-id="a4480-149">A Parameters deklaráció a házirend-definícióban.</span><span class="sxs-lookup"><span data-stu-id="a4480-149">The parameters declaration for policy definition.</span></span> <span data-ttu-id="a4480-150">Ez lehet elérési út a Parameters deklarációt tartalmazó fájlnév vagy URI-azonosítóhoz, illetve a Parameters deklaráció karakterláncként való eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="a4480-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="a4480-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4480-151">CommonParameters</span></span>
<span data-ttu-id="a4480-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4480-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4480-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4480-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4480-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4480-154">INPUTS</span></span>

## <span data-ttu-id="a4480-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4480-155">OUTPUTS</span></span>

### <span data-ttu-id="a4480-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a4480-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a4480-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4480-157">NOTES</span></span>

## <span data-ttu-id="a4480-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4480-158">RELATED LINKS</span></span>

[<span data-ttu-id="a4480-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a4480-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="a4480-160">Új – AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a4480-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="a4480-161">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a4480-161">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


