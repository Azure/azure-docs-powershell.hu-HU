---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: 63ab8e9004b993429af31cb54e360c0b6d9854fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503215"
---
# <span data-ttu-id="8424c-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8424c-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="8424c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8424c-102">SYNOPSIS</span></span>
<span data-ttu-id="8424c-103">Házirend-definíciókat kap.</span><span class="sxs-lookup"><span data-stu-id="8424c-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8424c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8424c-104">SYNTAX</span></span>

### <span data-ttu-id="8424c-105">A lista minden házirend-definíciós paraméterét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8424c-105">The list all policy definitions parameter set.</span></span> <span data-ttu-id="8424c-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="8424c-106">(Default)</span></span>
```
Get-AzureRmPolicyDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8424c-107">A Policy definition Name paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="8424c-107">The policy definition name parameter set.</span></span>
```
Get-AzureRmPolicyDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8424c-108">A házirend-definíciós azonosító paraméter beállítása.</span><span class="sxs-lookup"><span data-stu-id="8424c-108">The policy definition Id parameter set.</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8424c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="8424c-109">DESCRIPTION</span></span>
<span data-ttu-id="8424c-110">A **Get-AzureRmPolicyDefinition** parancsmag az összes házirend-definíciót vagy egy olyan konkrét házirend-definíciót kapja, amelyet név vagy azonosító szerint azonosítottak.</span><span class="sxs-lookup"><span data-stu-id="8424c-110">The **Get-AzureRmPolicyDefinition** cmdlet gets all the policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="8424c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="8424c-111">EXAMPLES</span></span>

### <span data-ttu-id="8424c-112">Példa 1: az összes házirend-definíció beolvasása</span><span class="sxs-lookup"><span data-stu-id="8424c-112">Example 1: Get all policy definition</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition
```

<span data-ttu-id="8424c-113">Ez a parancs az összes házirend-definíciót megkapja.</span><span class="sxs-lookup"><span data-stu-id="8424c-113">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="8424c-114">2. példa: házirend-definíció beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="8424c-114">Example 2: Get policy definition by name</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="8424c-115">Ez a parancs a VMPolicyDefinition nevű házirend-definíciót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8424c-115">This command gets the policy definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="8424c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8424c-116">PARAMETERS</span></span>

### <span data-ttu-id="8424c-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8424c-117">-ApiVersion</span></span>
<span data-ttu-id="8424c-118">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8424c-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8424c-119">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="8424c-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8424c-120">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="8424c-120">-Id</span></span>
<span data-ttu-id="8424c-121">Annak a házirend-definíciónak a teljesen minősített erőforrás-AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="8424c-121">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8424c-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8424c-122">-InformationAction</span></span>
<span data-ttu-id="8424c-123">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="8424c-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8424c-124">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8424c-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8424c-125">Folytassa</span><span class="sxs-lookup"><span data-stu-id="8424c-125">Continue</span></span>
- <span data-ttu-id="8424c-126">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="8424c-126">Ignore</span></span>
- <span data-ttu-id="8424c-127">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="8424c-127">Inquire</span></span>
- <span data-ttu-id="8424c-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8424c-128">SilentlyContinue</span></span>
- <span data-ttu-id="8424c-129">állj</span><span class="sxs-lookup"><span data-stu-id="8424c-129">Stop</span></span>
- <span data-ttu-id="8424c-130">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="8424c-130">Suspend</span></span>

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

### <span data-ttu-id="8424c-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8424c-131">-InformationVariable</span></span>
<span data-ttu-id="8424c-132">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="8424c-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8424c-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8424c-133">-Name</span></span>
<span data-ttu-id="8424c-134">Annak a házirend-definíciónak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="8424c-134">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8424c-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="8424c-135">-Pre</span></span>
<span data-ttu-id="8424c-136">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="8424c-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8424c-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8424c-137">-DefaultProfile</span></span>
<span data-ttu-id="8424c-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8424c-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8424c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8424c-139">CommonParameters</span></span>
<span data-ttu-id="8424c-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8424c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8424c-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8424c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8424c-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8424c-142">INPUTS</span></span>

## <span data-ttu-id="8424c-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8424c-143">OUTPUTS</span></span>

### <span data-ttu-id="8424c-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8424c-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8424c-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8424c-145">NOTES</span></span>

## <span data-ttu-id="8424c-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8424c-146">RELATED LINKS</span></span>

[<span data-ttu-id="8424c-147">Új – AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8424c-147">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="8424c-148">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8424c-148">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="8424c-149">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8424c-149">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


