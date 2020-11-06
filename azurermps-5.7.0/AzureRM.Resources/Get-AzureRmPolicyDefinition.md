---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: d9d79374e426c6d895fbfcef957da20ed9721f70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501423"
---
# <span data-ttu-id="84694-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="84694-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="84694-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84694-102">SYNOPSIS</span></span>
<span data-ttu-id="84694-103">Házirend-definíciókat kap.</span><span class="sxs-lookup"><span data-stu-id="84694-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84694-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84694-104">SYNTAX</span></span>

### <span data-ttu-id="84694-105">GetAllPolicyDefinitions (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="84694-105">GetAllPolicyDefinitions (Default)</span></span>
```
Get-AzureRmPolicyDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="84694-106">GetByPolicyDefintionName</span><span class="sxs-lookup"><span data-stu-id="84694-106">GetByPolicyDefintionName</span></span>
```
Get-AzureRmPolicyDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="84694-107">GetByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="84694-107">GetByPolicyDefinitionId</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="84694-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="84694-108">DESCRIPTION</span></span>
<span data-ttu-id="84694-109">A **Get-AzureRmPolicyDefinition** parancsmag az összes házirend-definíciót vagy egy olyan konkrét házirend-definíciót kapja, amelyet név vagy azonosító szerint azonosítottak.</span><span class="sxs-lookup"><span data-stu-id="84694-109">The **Get-AzureRmPolicyDefinition** cmdlet gets all the policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="84694-110">Példák</span><span class="sxs-lookup"><span data-stu-id="84694-110">EXAMPLES</span></span>

### <span data-ttu-id="84694-111">Példa 1: az összes házirend-definíció beolvasása</span><span class="sxs-lookup"><span data-stu-id="84694-111">Example 1: Get all policy definition</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition
```

<span data-ttu-id="84694-112">Ez a parancs az összes házirend-definíciót megkapja.</span><span class="sxs-lookup"><span data-stu-id="84694-112">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="84694-113">2. példa: házirend-definíció beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="84694-113">Example 2: Get policy definition by name</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="84694-114">Ez a parancs a VMPolicyDefinition nevű házirend-definíciót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="84694-114">This command gets the policy definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="84694-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84694-115">PARAMETERS</span></span>

### <span data-ttu-id="84694-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="84694-116">-ApiVersion</span></span>
<span data-ttu-id="84694-117">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="84694-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="84694-118">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="84694-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="84694-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84694-119">-DefaultProfile</span></span>
<span data-ttu-id="84694-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="84694-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84694-121">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="84694-121">-Id</span></span>
<span data-ttu-id="84694-122">Annak a házirend-definíciónak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="84694-122">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="84694-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="84694-123">-InformationAction</span></span>
<span data-ttu-id="84694-124">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="84694-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="84694-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="84694-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="84694-126">Folytassa</span><span class="sxs-lookup"><span data-stu-id="84694-126">Continue</span></span>
- <span data-ttu-id="84694-127">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="84694-127">Ignore</span></span>
- <span data-ttu-id="84694-128">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="84694-128">Inquire</span></span>
- <span data-ttu-id="84694-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="84694-129">SilentlyContinue</span></span>
- <span data-ttu-id="84694-130">állj</span><span class="sxs-lookup"><span data-stu-id="84694-130">Stop</span></span>
- <span data-ttu-id="84694-131">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="84694-131">Suspend</span></span>

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

### <span data-ttu-id="84694-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="84694-132">-InformationVariable</span></span>
<span data-ttu-id="84694-133">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="84694-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="84694-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="84694-134">-Name</span></span>
<span data-ttu-id="84694-135">Annak a házirend-definíciónak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="84694-135">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="84694-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="84694-136">-Pre</span></span>
<span data-ttu-id="84694-137">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="84694-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="84694-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84694-138">CommonParameters</span></span>
<span data-ttu-id="84694-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84694-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84694-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84694-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84694-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84694-141">INPUTS</span></span>

### <span data-ttu-id="84694-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="84694-142">None</span></span>
<span data-ttu-id="84694-143">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="84694-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="84694-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84694-144">OUTPUTS</span></span>

### <span data-ttu-id="84694-145">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="84694-145">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="84694-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84694-146">NOTES</span></span>

## <span data-ttu-id="84694-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84694-147">RELATED LINKS</span></span>

[<span data-ttu-id="84694-148">Új – AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="84694-148">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="84694-149">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="84694-149">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="84694-150">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="84694-150">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


