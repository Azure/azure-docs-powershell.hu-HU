---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
ms.openlocfilehash: 5140219c5392a7fb9c727998ae248d600edfde23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501640"
---
# <span data-ttu-id="6a910-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6a910-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="6a910-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a910-102">SYNOPSIS</span></span>
<span data-ttu-id="6a910-103">Házirend-definíciót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6a910-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a910-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a910-104">SYNTAX</span></span>

```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6a910-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a910-105">DESCRIPTION</span></span>
<span data-ttu-id="6a910-106">A **New-AzureRmPolicyDefinition** parancsmag olyan házirend-definíciót hoz létre, amely egy JavaScript-objektum formátumú (JSON) formátumú házirend-szabályt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="6a910-106">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="6a910-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6a910-107">EXAMPLES</span></span>

### <span data-ttu-id="6a910-108">Példa 1: házirend-definíció létrehozása házirendfájl használatával</span><span class="sxs-lookup"><span data-stu-id="6a910-108">Example 1: Create a policy definition by using a policy file</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -Policy C:\VMPolicy.json
```

<span data-ttu-id="6a910-109">Ez a parancs létrehoz egy VMPolicyDefinition nevű házirend-definíciót, amely a C:\VMPolicy.jsban megadott házirend-szabályt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6a910-109">This command creates a policy definition named VMPolicyDefinition that contains the policy rule specified in C:\VMPolicy.json.</span></span>

### <span data-ttu-id="6a910-110">2. példa: házirend-definíció létrehozása szövegközi</span><span class="sxs-lookup"><span data-stu-id="6a910-110">Example 2: Create a policy definition inline</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -DisplayName "Virtual Machine policy definition" -Policy "{""if"":{""source"":""action"",""equals"":""Microsoft.Compute/virtualMachines/write""},""then"":{""effect"":""deny""}}"
```

<span data-ttu-id="6a910-111">Ez a parancs létrehoz egy VMPolicyDefinition nevű házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="6a910-111">This command creates a policy definition named VMPolicyDefinition.</span></span>
<span data-ttu-id="6a910-112">A parancs érvényes JSON formátumú karakterláncként adja meg a házirendet.</span><span class="sxs-lookup"><span data-stu-id="6a910-112">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="6a910-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a910-113">PARAMETERS</span></span>

### <span data-ttu-id="6a910-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6a910-114">-ApiVersion</span></span>
<span data-ttu-id="6a910-115">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a910-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6a910-116">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="6a910-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6a910-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="6a910-117">-Description</span></span>
<span data-ttu-id="6a910-118">A házirend definíciójának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a910-118">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="6a910-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6a910-119">-DisplayName</span></span>
<span data-ttu-id="6a910-120">A házirend-definíció megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a910-120">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="6a910-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6a910-121">-InformationAction</span></span>
<span data-ttu-id="6a910-122">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="6a910-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6a910-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6a910-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a910-124">Folytassa</span><span class="sxs-lookup"><span data-stu-id="6a910-124">Continue</span></span>
- <span data-ttu-id="6a910-125">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="6a910-125">Ignore</span></span>
- <span data-ttu-id="6a910-126">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="6a910-126">Inquire</span></span>
- <span data-ttu-id="6a910-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6a910-127">SilentlyContinue</span></span>
- <span data-ttu-id="6a910-128">állj</span><span class="sxs-lookup"><span data-stu-id="6a910-128">Stop</span></span>
- <span data-ttu-id="6a910-129">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="6a910-129">Suspend</span></span>

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

### <span data-ttu-id="6a910-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6a910-130">-InformationVariable</span></span>
<span data-ttu-id="6a910-131">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="6a910-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6a910-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6a910-132">-Name</span></span>
<span data-ttu-id="6a910-133">A házirend-definíció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a910-133">Specifies a name for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a910-134">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="6a910-134">-Parameter</span></span>
<span data-ttu-id="6a910-135">A Parameters deklaráció a házirend-definícióban.</span><span class="sxs-lookup"><span data-stu-id="6a910-135">The parameters declaration for policy definition.</span></span> <span data-ttu-id="6a910-136">Ez lehet a Parameters deklarációt vagy a Parameters deklarációt karakterláncként tartalmazó fájlnév elérési útja.</span><span class="sxs-lookup"><span data-stu-id="6a910-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="6a910-137">-Házirend</span><span class="sxs-lookup"><span data-stu-id="6a910-137">-Policy</span></span>
<span data-ttu-id="6a910-138">A házirend-definíció szabályait adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a910-138">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="6a910-139">Megadhatja a. JSON fájlok elérési útját vagy a JSON formátumú házirendet tartalmazó karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="6a910-139">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a910-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="6a910-140">-Pre</span></span>
<span data-ttu-id="6a910-141">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="6a910-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6a910-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a910-142">-DefaultProfile</span></span>
<span data-ttu-id="6a910-143">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a910-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a910-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="6a910-144">-Metadata</span></span>
<span data-ttu-id="6a910-145">A házirend-definíció metaadatai.</span><span class="sxs-lookup"><span data-stu-id="6a910-145">The metadata for policy definition.</span></span> <span data-ttu-id="6a910-146">Ez lehet a metaadatokat tartalmazó fájlnév vagy a metaadatok karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="6a910-146">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="6a910-147">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="6a910-147">-Mode</span></span>
<span data-ttu-id="6a910-148">A házirend definíciójának üzemmódja.</span><span class="sxs-lookup"><span data-stu-id="6a910-148">The mode of the policy definition.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a910-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a910-149">CommonParameters</span></span>
<span data-ttu-id="6a910-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a910-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a910-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a910-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a910-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a910-152">INPUTS</span></span>

## <span data-ttu-id="6a910-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a910-153">OUTPUTS</span></span>

### <span data-ttu-id="6a910-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="6a910-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6a910-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a910-155">NOTES</span></span>

## <span data-ttu-id="6a910-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a910-156">RELATED LINKS</span></span>

[<span data-ttu-id="6a910-157">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6a910-157">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="6a910-158">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6a910-158">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="6a910-159">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6a910-159">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


