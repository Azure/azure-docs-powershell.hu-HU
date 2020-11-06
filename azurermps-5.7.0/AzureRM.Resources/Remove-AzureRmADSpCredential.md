---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
ms.openlocfilehash: bfda87b4a0810dc440da63949d17f52cf611fa19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502484"
---
# <span data-ttu-id="907fa-101">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="907fa-101">Remove-AzureRmADSpCredential</span></span>

## <span data-ttu-id="907fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="907fa-102">SYNOPSIS</span></span>
<span data-ttu-id="907fa-103">Hitelesítő adatok eltávolítása egy egyszerű szolgáltatótól.</span><span class="sxs-lookup"><span data-stu-id="907fa-103">Removes a credential from a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="907fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="907fa-104">SYNTAX</span></span>

### <span data-ttu-id="907fa-105">ObjectIdWithKeyIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="907fa-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="907fa-106">ObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="907fa-106">ObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="907fa-107">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="907fa-107">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="907fa-108">SPNWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="907fa-108">SPNWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="907fa-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="907fa-109">DESCRIPTION</span></span>
<span data-ttu-id="907fa-110">A Remove-AzureRmADSpCredential parancsmag használatával kompromisszum vagy a hitelesítő adatok kulcsának lejárati dátuma részeként eltávolíthatja a hitelesítő adatok kulcsát a megbízótól.</span><span class="sxs-lookup"><span data-stu-id="907fa-110">The Remove-AzureRmADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="907fa-111">A rendszer az objektumazonosító vagy az egyszerű szolgáltatásnév (SPN) megadásával azonosítja a megbízót.</span><span class="sxs-lookup"><span data-stu-id="907fa-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>

<span data-ttu-id="907fa-112">Az eltávolítani kívánt hitelesítő adatokat a program annak AZONOSÍTÓját azonosítja, ha az egyes hitelesítő adatok törlődnek, vagy egy "minden" kapcsolóval törli a szolgáltatóhoz társított összes hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="907fa-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="907fa-113">Példák</span><span class="sxs-lookup"><span data-stu-id="907fa-113">EXAMPLES</span></span>

### <span data-ttu-id="907fa-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="907fa-114">Example 1</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="907fa-115">Ez a parancs eltávolítja a hitelesítő kulcsot egy egyszerű szolgáltatótól.</span><span class="sxs-lookup"><span data-stu-id="907fa-115">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="907fa-116">Ebben a példában a "9044423a-60a3-45ac--9ab1 – 09534157ebb" azonosítójú kulcs törlődik a szolgáltatótól.</span><span class="sxs-lookup"><span data-stu-id="907fa-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the service principal.</span></span>

### <span data-ttu-id="907fa-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="907fa-117">Example 2</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123 -All
```

<span data-ttu-id="907fa-118">Ez a parancs eltávolítja a hitelesítő kulcsot egy egyszerű szolgáltatótól.</span><span class="sxs-lookup"><span data-stu-id="907fa-118">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="907fa-119">Ebben a példában az összes hitelesítő adat törlődik a szolgáltatás fő nevéhez társított szolgáltatótól: " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="907fa-119">In this example, all credentials will be removed from the service principal associated with the service principal name "http://test123".</span></span>

## <span data-ttu-id="907fa-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="907fa-120">PARAMETERS</span></span>

### <span data-ttu-id="907fa-121">-All (mind)</span><span class="sxs-lookup"><span data-stu-id="907fa-121">-All</span></span>
<span data-ttu-id="907fa-122">Váltson a szolgáltatóhoz társított összes hitelesítő adat eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="907fa-122">Switch to remove all the credentials associated with the service principal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ObjectIdWithAllParameterSet, SPNWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="907fa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="907fa-123">-DefaultProfile</span></span>
<span data-ttu-id="907fa-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="907fa-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="907fa-125">-Force</span><span class="sxs-lookup"><span data-stu-id="907fa-125">-Force</span></span>
<span data-ttu-id="907fa-126">Váltás a hitelesítő adatok törlésére megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="907fa-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="907fa-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="907fa-127">-KeyId</span></span>
<span data-ttu-id="907fa-128">Az eltávolítandó hitelesítőadat-kulcsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="907fa-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="907fa-129">A megbízó kulcs-azonosítói a Get-AzureRmADSpCredential parancsmag használatával szerezhetők be.</span><span class="sxs-lookup"><span data-stu-id="907fa-129">The key Ids for a service principal can be obtained using the Get-AzureRmADSpCredential cmdlet.</span></span>

```yaml
Type: Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="907fa-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="907fa-130">-ObjectId</span></span>
<span data-ttu-id="907fa-131">Annak az objektumnak az azonosítója a szolgáltatónál, akinek a hitelesítő adatait el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="907fa-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ObjectIdWithKeyIdParameterSet, ObjectIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="907fa-132">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="907fa-132">-ServicePrincipalName</span></span>
<span data-ttu-id="907fa-133">A szolgáltatás megbízójának neve (SPN) a hitelesítő adatok eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="907fa-133">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithKeyIdParameterSet, SPNWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="907fa-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="907fa-134">-Confirm</span></span>
<span data-ttu-id="907fa-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="907fa-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="907fa-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="907fa-136">-WhatIf</span></span>
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

### <span data-ttu-id="907fa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="907fa-137">CommonParameters</span></span>
<span data-ttu-id="907fa-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="907fa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="907fa-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="907fa-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="907fa-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="907fa-140">INPUTS</span></span>

### <span data-ttu-id="907fa-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="907fa-141">None</span></span>
<span data-ttu-id="907fa-142">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="907fa-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="907fa-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="907fa-143">OUTPUTS</span></span>

## <span data-ttu-id="907fa-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="907fa-144">NOTES</span></span>

## <span data-ttu-id="907fa-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="907fa-145">RELATED LINKS</span></span>

[<span data-ttu-id="907fa-146">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="907fa-146">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="907fa-147">Új – AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="907fa-147">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="907fa-148">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="907fa-148">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

