---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: d7e01294836145b09844fa3bca49421df20f67d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501404"
---
# <span data-ttu-id="f1e94-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f1e94-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="f1e94-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1e94-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e94-103">Módosította a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="f1e94-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1e94-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1e94-104">SYNTAX</span></span>

### <span data-ttu-id="f1e94-105">SetByPolicyDefinitionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f1e94-105">SetByPolicyDefinitionName (Default)</span></span>
```
Set-AzureRmPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f1e94-106">GetByPolicyDefintionName</span><span class="sxs-lookup"><span data-stu-id="f1e94-106">GetByPolicyDefintionName</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f1e94-107">GetByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="f1e94-107">GetByPolicyDefinitionId</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f1e94-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1e94-108">DESCRIPTION</span></span>
<span data-ttu-id="f1e94-109">A **set-AzureRmPolicyDefinition** parancsmag módosította a házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="f1e94-109">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="f1e94-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f1e94-110">EXAMPLES</span></span>

### <span data-ttu-id="f1e94-111">Példa 1: házirend-definíció leírásának frissítése</span><span class="sxs-lookup"><span data-stu-id="f1e94-111">Example 1: Update the description of a policy definition</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
PS C:\> Set-AzureRmPolicyDefinition -Id $Policy.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="f1e94-112">Az első parancs az Get-AzureRmPolicyDefinition parancsmag használatával megkapja a VMPolicyDefinition nevű házirend-definíciót.</span><span class="sxs-lookup"><span data-stu-id="f1e94-112">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="f1e94-113">A parancs az objektumot a $PolicyDefinition változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f1e94-113">The command stores that object in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="f1e94-114">A második parancs frissíti a $PolicyDefinition **ResourceId** tulajdonsága által azonosított házirend-definíció leírását.</span><span class="sxs-lookup"><span data-stu-id="f1e94-114">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="f1e94-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1e94-115">PARAMETERS</span></span>

### <span data-ttu-id="f1e94-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f1e94-116">-ApiVersion</span></span>
<span data-ttu-id="f1e94-117">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1e94-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f1e94-118">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="f1e94-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e94-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e94-119">-DefaultProfile</span></span>
<span data-ttu-id="f1e94-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f1e94-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e94-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f1e94-121">-Description</span></span>
<span data-ttu-id="f1e94-122">A házirend-definíció új leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1e94-122">Specifies a new description for the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e94-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f1e94-123">-DisplayName</span></span>
<span data-ttu-id="f1e94-124">A házirend-definíció új megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1e94-124">Specifies a new display name for the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e94-125">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f1e94-125">-Id</span></span>
<span data-ttu-id="f1e94-126">Annak a házirend-definíciónak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="f1e94-126">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e94-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f1e94-127">-InformationAction</span></span>
<span data-ttu-id="f1e94-128">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="f1e94-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f1e94-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f1e94-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1e94-130">Folytassa</span><span class="sxs-lookup"><span data-stu-id="f1e94-130">Continue</span></span>
- <span data-ttu-id="f1e94-131">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="f1e94-131">Ignore</span></span>
- <span data-ttu-id="f1e94-132">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="f1e94-132">Inquire</span></span>
- <span data-ttu-id="f1e94-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f1e94-133">SilentlyContinue</span></span>
- <span data-ttu-id="f1e94-134">állj</span><span class="sxs-lookup"><span data-stu-id="f1e94-134">Stop</span></span>
- <span data-ttu-id="f1e94-135">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="f1e94-135">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e94-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f1e94-136">-InformationVariable</span></span>
<span data-ttu-id="f1e94-137">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="f1e94-137">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e94-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f1e94-138">-Metadata</span></span>
<span data-ttu-id="f1e94-139">A házirend-definíció metaadatai.</span><span class="sxs-lookup"><span data-stu-id="f1e94-139">The metadata for policy definition.</span></span> <span data-ttu-id="f1e94-140">Ez lehet a metaadatokat tartalmazó fájlnév vagy a metaadatok karakterláncként való elérési útja.</span><span class="sxs-lookup"><span data-stu-id="f1e94-140">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e94-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f1e94-141">-Name</span></span>
<span data-ttu-id="f1e94-142">Annak a házirend-definíciónak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="f1e94-142">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefintionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e94-143">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="f1e94-143">-Parameter</span></span>
<span data-ttu-id="f1e94-144">A Parameters deklaráció a házirend-definícióban.</span><span class="sxs-lookup"><span data-stu-id="f1e94-144">The parameters declaration for policy definition.</span></span> <span data-ttu-id="f1e94-145">Ez lehet elérési út a Parameters deklarációt tartalmazó fájlnév vagy URI-azonosítóhoz, illetve a Parameters deklaráció karakterláncként való eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="f1e94-145">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e94-146">-Házirend</span><span class="sxs-lookup"><span data-stu-id="f1e94-146">-Policy</span></span>
<span data-ttu-id="f1e94-147">A házirend-definíció új házirend-szabályát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1e94-147">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="f1e94-148">Megadhatja a. JSON fájlok elérési útját, vagy a házirendet a JavaScript-objektum formátumban (JSON) tartalmazó karakterláncban.</span><span class="sxs-lookup"><span data-stu-id="f1e94-148">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e94-149">-Pre</span><span class="sxs-lookup"><span data-stu-id="f1e94-149">-Pre</span></span>
<span data-ttu-id="f1e94-150">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="f1e94-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e94-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e94-151">CommonParameters</span></span>
<span data-ttu-id="f1e94-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1e94-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e94-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1e94-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e94-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1e94-154">INPUTS</span></span>

### <span data-ttu-id="f1e94-155">Nincs</span><span class="sxs-lookup"><span data-stu-id="f1e94-155">None</span></span>
<span data-ttu-id="f1e94-156">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f1e94-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f1e94-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1e94-157">OUTPUTS</span></span>

### <span data-ttu-id="f1e94-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f1e94-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f1e94-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1e94-159">NOTES</span></span>

## <span data-ttu-id="f1e94-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1e94-160">RELATED LINKS</span></span>

[<span data-ttu-id="f1e94-161">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f1e94-161">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="f1e94-162">Új – AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f1e94-162">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="f1e94-163">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f1e94-163">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


