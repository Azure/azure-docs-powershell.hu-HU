---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
ms.openlocfilehash: 0cfcb2713eaac255f625b09c0ba81883242f48aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493024"
---
# <span data-ttu-id="e4ede-101">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e4ede-101">Remove-AzureRmADAppCredential</span></span>

## <span data-ttu-id="e4ede-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4ede-102">SYNOPSIS</span></span>
<span data-ttu-id="e4ede-103">Hitelesítő adatok eltávolítása egy alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="e4ede-103">Removes a credential from an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4ede-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4ede-104">SYNTAX</span></span>

### <span data-ttu-id="e4ede-105">ApplicationObjectIdWithKeyIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e4ede-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4ede-106">ApplicationObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4ede-106">ApplicationObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4ede-107">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4ede-107">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4ede-108">ApplicationIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4ede-108">ApplicationIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4ede-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4ede-109">DESCRIPTION</span></span>
<span data-ttu-id="e4ede-110">A Remove-AzureRmADAppCredential parancsmagot kiegyezéssel vagy a hitelesítő adatok kulcsának lejárati időpontjának részeként lehet eltávolítani egy alkalmazás hitelesítő kulcsával.</span><span class="sxs-lookup"><span data-stu-id="e4ede-110">The Remove-AzureRmADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="e4ede-111">Az alkalmazás azonosítása az objektum-azonosító vagy a AppId megadásával történik.</span><span class="sxs-lookup"><span data-stu-id="e4ede-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="e4ede-112">Az eltávolítani kívánt hitelesítő adatokat a rendszer a kulcs azonosítójával azonosítja, ha az egyes hitelesítő adatok törlődnek, vagy egy "minden" kapcsolóval az alkalmazáshoz társított összes hitelesítő adatok törlődnek.</span><span class="sxs-lookup"><span data-stu-id="e4ede-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the application.</span></span>

## <span data-ttu-id="e4ede-113">Példák</span><span class="sxs-lookup"><span data-stu-id="e4ede-113">EXAMPLES</span></span>

### <span data-ttu-id="e4ede-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e4ede-114">Example 1</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="e4ede-115">Ez a parancs eltávolítja a hitelesítő kulcsot egy alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="e4ede-115">This command removes a credential key from an application.</span></span>
<span data-ttu-id="e4ede-116">Ebben a példában a "9044423a-60a3-45ac--9ab1 – 09534157ebb" azonosítójú kulcs törlődik az alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="e4ede-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the application.</span></span>

### <span data-ttu-id="e4ede-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="e4ede-117">Example 2</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -All
```

<span data-ttu-id="e4ede-118">Ez a parancs eltávolítja a hitelesítő kulcsot egy alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="e4ede-118">This command removes a credential key from an application.</span></span>
<span data-ttu-id="e4ede-119">Ebben a példában a hitelesítő adatok törlődnek a "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58" applicationId társított alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="e4ede-119">In this example, all credentials will be removed from the application associated with the applicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span></span>

## <span data-ttu-id="e4ede-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4ede-120">PARAMETERS</span></span>

### <span data-ttu-id="e4ede-121">-All (mind)</span><span class="sxs-lookup"><span data-stu-id="e4ede-121">-All</span></span>
<span data-ttu-id="e4ede-122">Váltson az alkalmazáshoz társított összes hitelesítő adat eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="e4ede-122">Switch to remove all the credentials associated with the application.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ApplicationObjectIdWithAllParameterSet, ApplicationIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4ede-123">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e4ede-123">-ApplicationId</span></span>
<span data-ttu-id="e4ede-124">Az alkalmazás azonosítója a hitelesítő adatok eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="e4ede-124">The id of the application to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithKeyIdParameterSet, ApplicationIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4ede-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4ede-125">-DefaultProfile</span></span>
<span data-ttu-id="e4ede-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e4ede-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4ede-127">-Force</span><span class="sxs-lookup"><span data-stu-id="e4ede-127">-Force</span></span>
<span data-ttu-id="e4ede-128">Váltás a hitelesítő adatok törlésére megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="e4ede-128">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="e4ede-129">-KeyId</span><span class="sxs-lookup"><span data-stu-id="e4ede-129">-KeyId</span></span>
<span data-ttu-id="e4ede-130">Az eltávolítandó hitelesítőadat-kulcsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4ede-130">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="e4ede-131">Az alkalmazáshoz tartozó kulcs-azonosítók az Get-AzureRmADAppCredential parancsmag használatával szerezhetők be.</span><span class="sxs-lookup"><span data-stu-id="e4ede-131">The key Ids for the application can be obtained using the Get-AzureRmADAppCredential cmdlet.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4ede-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e4ede-132">-ObjectId</span></span>
<span data-ttu-id="e4ede-133">Az alkalmazás Object ID-je a hitelesítő adatok eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="e4ede-133">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationObjectIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4ede-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e4ede-134">-Confirm</span></span>
<span data-ttu-id="e4ede-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e4ede-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4ede-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4ede-136">-WhatIf</span></span>
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

### <span data-ttu-id="e4ede-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4ede-137">CommonParameters</span></span>
<span data-ttu-id="e4ede-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4ede-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4ede-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4ede-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4ede-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4ede-140">INPUTS</span></span>

### <span data-ttu-id="e4ede-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="e4ede-141">None</span></span>
<span data-ttu-id="e4ede-142">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e4ede-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4ede-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4ede-143">OUTPUTS</span></span>

## <span data-ttu-id="e4ede-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4ede-144">NOTES</span></span>

## <span data-ttu-id="e4ede-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4ede-145">RELATED LINKS</span></span>

[<span data-ttu-id="e4ede-146">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e4ede-146">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="e4ede-147">Új – AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e4ede-147">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="e4ede-148">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="e4ede-148">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)
