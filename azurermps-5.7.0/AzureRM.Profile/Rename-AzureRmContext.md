---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/rename-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
ms.openlocfilehash: 6163602d2975a9ec77e572ec0033ef2c626d2cfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500471"
---
# <span data-ttu-id="81b4b-101">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="81b4b-101">Rename-AzureRmContext</span></span>

## <span data-ttu-id="81b4b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81b4b-102">SYNOPSIS</span></span>
<span data-ttu-id="81b4b-103">Azure-környezet átnevezése</span><span class="sxs-lookup"><span data-stu-id="81b4b-103">Rename an Azure context.</span></span>  <span data-ttu-id="81b4b-104">Alapértelmezés szerint a kontextusokat felhasználói fiók és előfizetés szerint nevezi el a program.</span><span class="sxs-lookup"><span data-stu-id="81b4b-104">By default contexts are named by user account and subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81b4b-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81b4b-105">SYNTAX</span></span>

### <span data-ttu-id="81b4b-106">RenameByInputObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="81b4b-106">RenameByInputObject (Default)</span></span>
```
Rename-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="81b4b-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="81b4b-107">RenameByName</span></span>
```
Rename-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="81b4b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="81b4b-108">DESCRIPTION</span></span>
<span data-ttu-id="81b4b-109">Azure-környezet átnevezése</span><span class="sxs-lookup"><span data-stu-id="81b4b-109">Rename an Azure context.</span></span>  <span data-ttu-id="81b4b-110">Alapértelmezés szerint a kontextusokat felhasználói fiók és előfizetés szerint nevezi el a program.</span><span class="sxs-lookup"><span data-stu-id="81b4b-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="81b4b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="81b4b-111">EXAMPLES</span></span>

### <span data-ttu-id="81b4b-112">Környezet átnevezése névvel ellátott paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="81b4b-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzureRmContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="81b4b-113">A " user1@contoso.org '" előfizetés "12345-6789-2345-3567890" "munka" nevű környezetének átnevezése</span><span class="sxs-lookup"><span data-stu-id="81b4b-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="81b4b-114">A parancs elvégzése után a környezetet a "Select-AzureRmContext" munkával is megtalálhatja.</span><span class="sxs-lookup"><span data-stu-id="81b4b-114">After this command, you will be able to target the context using 'Select-AzureRmContext Work'.</span></span>  <span data-ttu-id="81b4b-115">Figyelje meg, hogy a TAB billentyűvel a "SourceName" értékek között a TAB billentyűvel válthat.</span><span class="sxs-lookup"><span data-stu-id="81b4b-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="81b4b-116">Környezet átnevezése az elhelyezési paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="81b4b-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzureRmContext "My context" "Work"
```

<span data-ttu-id="81b4b-117">Nevezze át a "saját környezet" nevű környezetet a "munka" értékre.</span><span class="sxs-lookup"><span data-stu-id="81b4b-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="81b4b-118">A parancs elvégzése után Select-AzureRmContext-munkakörnyezettel megcélzott környezete</span><span class="sxs-lookup"><span data-stu-id="81b4b-118">After this command, you will be able to target the context using Select-AzureRmContext Work</span></span>

## <span data-ttu-id="81b4b-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81b4b-119">PARAMETERS</span></span>

### <span data-ttu-id="81b4b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81b4b-120">-DefaultProfile</span></span>
<span data-ttu-id="81b4b-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="81b4b-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81b4b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="81b4b-122">-Force</span></span>
<span data-ttu-id="81b4b-123">A környezet átnevezése akkor is, ha már létezik a cél környezete</span><span class="sxs-lookup"><span data-stu-id="81b4b-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="81b4b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81b4b-124">-InputObject</span></span>
<span data-ttu-id="81b4b-125">Egy környezeti objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="81b4b-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: RenameByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81b4b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81b4b-126">-PassThru</span></span>
<span data-ttu-id="81b4b-127">Adja vissza az átnevezett környezetet.</span><span class="sxs-lookup"><span data-stu-id="81b4b-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="81b4b-128">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="81b4b-128">-Scope</span></span>
<span data-ttu-id="81b4b-129">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="81b4b-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b4b-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="81b4b-130">-SourceName</span></span>
<span data-ttu-id="81b4b-131">A környezet neve</span><span class="sxs-lookup"><span data-stu-id="81b4b-131">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: RenameByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b4b-132">-Cél</span><span class="sxs-lookup"><span data-stu-id="81b4b-132">-TargetName</span></span>
<span data-ttu-id="81b4b-133">A környezet új neve</span><span class="sxs-lookup"><span data-stu-id="81b4b-133">The new name of the context</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b4b-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="81b4b-134">-Confirm</span></span>
<span data-ttu-id="81b4b-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81b4b-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b4b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81b4b-136">-WhatIf</span></span>
<span data-ttu-id="81b4b-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="81b4b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81b4b-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81b4b-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b4b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b4b-139">CommonParameters</span></span>
<span data-ttu-id="81b4b-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81b4b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b4b-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81b4b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b4b-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81b4b-142">INPUTS</span></span>

### <span data-ttu-id="81b4b-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="81b4b-143">None</span></span>

## <span data-ttu-id="81b4b-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81b4b-144">OUTPUTS</span></span>

### <span data-ttu-id="81b4b-145">Microsoft. Azure. Command. profil. models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="81b4b-145">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="81b4b-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81b4b-146">NOTES</span></span>

## <span data-ttu-id="81b4b-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81b4b-147">RELATED LINKS</span></span>

