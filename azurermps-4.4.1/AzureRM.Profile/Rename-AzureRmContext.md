---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
ms.openlocfilehash: 9c9c0c3c52f610c0bb2c0198e9995cf2804b2b24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680510"
---
# <span data-ttu-id="e2397-101">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="e2397-101">Rename-AzureRmContext</span></span>

## <span data-ttu-id="e2397-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2397-102">SYNOPSIS</span></span>
<span data-ttu-id="e2397-103">Azure-környezet átnevezése</span><span class="sxs-lookup"><span data-stu-id="e2397-103">Rename an Azure context.</span></span>  <span data-ttu-id="e2397-104">Alapértelmezés szerint a kontextusokat felhasználói fiók és előfizetés szerint nevezi el a program.</span><span class="sxs-lookup"><span data-stu-id="e2397-104">By default contexts are named by user account and subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2397-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2397-105">SYNTAX</span></span>

### <span data-ttu-id="e2397-106">Beviteli objektum (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e2397-106">Input Object (Default)</span></span>
```
Rename-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="e2397-107">Környezeti név</span><span class="sxs-lookup"><span data-stu-id="e2397-107">Context Name</span></span>
```
Rename-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="e2397-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2397-108">DESCRIPTION</span></span>
<span data-ttu-id="e2397-109">Azure-környezet átnevezése</span><span class="sxs-lookup"><span data-stu-id="e2397-109">Rename an Azure context.</span></span>  <span data-ttu-id="e2397-110">Alapértelmezés szerint a kontextusokat felhasználói fiók és előfizetés szerint nevezi el a program.</span><span class="sxs-lookup"><span data-stu-id="e2397-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="e2397-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e2397-111">EXAMPLES</span></span>

### <span data-ttu-id="e2397-112">Környezet átnevezése névvel ellátott paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="e2397-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzureRmContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="e2397-113">A " user1@contoso.org '" előfizetés "12345-6789-2345-3567890" "munka" nevű környezetének átnevezése</span><span class="sxs-lookup"><span data-stu-id="e2397-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="e2397-114">A parancs elvégzése után a környezetet a "Select-AzureRmContext" munkával is megtalálhatja.</span><span class="sxs-lookup"><span data-stu-id="e2397-114">After this command, you will be able to target the context using 'Select-AzureRmContext Work'.</span></span>  <span data-ttu-id="e2397-115">Figyelje meg, hogy a TAB billentyűvel a "SourceName" értékek között a TAB billentyűvel válthat.</span><span class="sxs-lookup"><span data-stu-id="e2397-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="e2397-116">Környezet átnevezése az elhelyezési paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="e2397-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzureRmContext "My context" "Work"
```

<span data-ttu-id="e2397-117">Nevezze át a "saját környezet" nevű környezetet a "munka" értékre.</span><span class="sxs-lookup"><span data-stu-id="e2397-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="e2397-118">A parancs elvégzése után Select-AzureRmContext-munkakörnyezettel megcélzott környezete</span><span class="sxs-lookup"><span data-stu-id="e2397-118">After this command, you will be able to target the context using Select-AzureRmContext Work</span></span>

## <span data-ttu-id="e2397-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2397-119">PARAMETERS</span></span>

### <span data-ttu-id="e2397-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2397-120">-DefaultProfile</span></span>
<span data-ttu-id="e2397-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e2397-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2397-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e2397-122">-Force</span></span>
<span data-ttu-id="e2397-123">A környezet átnevezése akkor is, ha már létezik a cél környezete</span><span class="sxs-lookup"><span data-stu-id="e2397-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="e2397-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2397-124">-InputObject</span></span>
<span data-ttu-id="e2397-125">Egy környezeti objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="e2397-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Input Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2397-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2397-126">-PassThru</span></span>
<span data-ttu-id="e2397-127">Adja vissza az átnevezett környezetet.</span><span class="sxs-lookup"><span data-stu-id="e2397-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="e2397-128">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="e2397-128">-Scope</span></span>
<span data-ttu-id="e2397-129">A környezeti változások hatókörét határozza meg, például a wheher módosítása csak a cusrrent folyamatra, illetve a felhasználó által indított összes munkamenetre érvényes.</span><span class="sxs-lookup"><span data-stu-id="e2397-129">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2397-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="e2397-130">-SourceName</span></span>
<span data-ttu-id="e2397-131">A környezet neve</span><span class="sxs-lookup"><span data-stu-id="e2397-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Context Name
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2397-132">-Cél</span><span class="sxs-lookup"><span data-stu-id="e2397-132">-TargetName</span></span>
<span data-ttu-id="e2397-133">A környezet új neve</span><span class="sxs-lookup"><span data-stu-id="e2397-133">The new name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2397-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e2397-134">-Confirm</span></span>
<span data-ttu-id="e2397-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e2397-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2397-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2397-136">-WhatIf</span></span>
<span data-ttu-id="e2397-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e2397-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2397-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e2397-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2397-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2397-139">CommonParameters</span></span>
<span data-ttu-id="e2397-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2397-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2397-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2397-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2397-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2397-142">INPUTS</span></span>

### <span data-ttu-id="e2397-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="e2397-143">None</span></span>

## <span data-ttu-id="e2397-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2397-144">OUTPUTS</span></span>

### <span data-ttu-id="e2397-145">Microsoft. Azure. Command. profil. models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="e2397-145">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="e2397-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2397-146">NOTES</span></span>

## <span data-ttu-id="e2397-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2397-147">RELATED LINKS</span></span>

