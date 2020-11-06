---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: b44d3bbf7c594f5f9114488b536d28fd17fe56c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501431"
---
# <span data-ttu-id="4c6ed-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4c6ed-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="4c6ed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c6ed-102">SYNOPSIS</span></span>
<span data-ttu-id="4c6ed-103">Felsorolja a meglévő Azure Active Directory-alkalmazásokat.</span><span class="sxs-lookup"><span data-stu-id="4c6ed-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c6ed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c6ed-104">SYNTAX</span></span>

### <span data-ttu-id="4c6ed-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4c6ed-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c6ed-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c6ed-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c6ed-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c6ed-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c6ed-108">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c6ed-108">ApplicationDisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c6ed-109">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c6ed-109">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c6ed-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c6ed-110">DESCRIPTION</span></span>
<span data-ttu-id="4c6ed-111">Felsorolja a meglévő Azure Active Directory-alkalmazásokat.</span><span class="sxs-lookup"><span data-stu-id="4c6ed-111">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="4c6ed-112">Az alkalmazások keresése a ObjectId, az ApplicationId, a IdentifierUri vagy a DisplayName segítségével végezhető el.</span><span class="sxs-lookup"><span data-stu-id="4c6ed-112">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="4c6ed-113">Ha nincs megadva paraméter, a program az összes alkalmazást beolvassa a bérlői webhelyre.</span><span class="sxs-lookup"><span data-stu-id="4c6ed-113">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="4c6ed-114">Példák</span><span class="sxs-lookup"><span data-stu-id="4c6ed-114">EXAMPLES</span></span>

### <span data-ttu-id="4c6ed-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4c6ed-115">Example 1</span></span>
```
PS E:\> Get-AzureRmADApplication
```

<span data-ttu-id="4c6ed-116">Felsorolja az összes alkalmazást bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="4c6ed-116">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="4c6ed-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="4c6ed-117">Example 2</span></span>
```
PS E:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="4c6ed-118">A "" azonosítóval kapja meg az alkalmazást http://mySecretApp1 .</span><span class="sxs-lookup"><span data-stu-id="4c6ed-118">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

## <span data-ttu-id="4c6ed-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c6ed-119">PARAMETERS</span></span>

### <span data-ttu-id="4c6ed-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4c6ed-120">-ApplicationId</span></span>
<span data-ttu-id="4c6ed-121">A lekérni kívánt alkalmazás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4c6ed-121">The application id of the application to fetch.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6ed-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c6ed-122">-DefaultProfile</span></span>
<span data-ttu-id="4c6ed-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4c6ed-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c6ed-124">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="4c6ed-124">-DisplayNameStartWith</span></span>
<span data-ttu-id="4c6ed-125">A megjelenítendő névvel kezdődő összes alkalmazás beolvasása</span><span class="sxs-lookup"><span data-stu-id="4c6ed-125">Fetch all applications starting with the display name.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6ed-126">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="4c6ed-126">-IdentifierUri</span></span>
<span data-ttu-id="4c6ed-127">A beolvasni kívánt alkalmazás egyedi azonosítójának URI azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4c6ed-127">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6ed-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4c6ed-128">-ObjectId</span></span>
<span data-ttu-id="4c6ed-129">A beolvasni kívánt alkalmazás objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4c6ed-129">The object id of the application to fetch.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6ed-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c6ed-130">CommonParameters</span></span>
<span data-ttu-id="4c6ed-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c6ed-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c6ed-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c6ed-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c6ed-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c6ed-133">INPUTS</span></span>

### <span data-ttu-id="4c6ed-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="4c6ed-134">None</span></span>
<span data-ttu-id="4c6ed-135">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="4c6ed-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4c6ed-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c6ed-136">OUTPUTS</span></span>

### <span data-ttu-id="4c6ed-137">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication]</span><span class="sxs-lookup"><span data-stu-id="4c6ed-137">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication]</span></span>

## <span data-ttu-id="4c6ed-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c6ed-138">NOTES</span></span>

## <span data-ttu-id="4c6ed-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c6ed-139">RELATED LINKS</span></span>

[<span data-ttu-id="4c6ed-140">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4c6ed-140">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="4c6ed-141">Új – AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4c6ed-141">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="4c6ed-142">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4c6ed-142">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="4c6ed-143">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4c6ed-143">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="4c6ed-144">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4c6ed-144">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="4c6ed-145">Új – AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4c6ed-145">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

