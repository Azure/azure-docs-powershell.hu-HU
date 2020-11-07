---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
ms.openlocfilehash: 4e7abd4a3b33f54e5a0ec0bdde01e3fe11da31c4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849053"
---
# <span data-ttu-id="0dc20-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="0dc20-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="0dc20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0dc20-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc20-103">Felsorolja a meglévő Azure Active Directory-alkalmazásokat.</span><span class="sxs-lookup"><span data-stu-id="0dc20-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0dc20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0dc20-104">SYNTAX</span></span>

### <span data-ttu-id="0dc20-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0dc20-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="0dc20-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc20-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="0dc20-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc20-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="0dc20-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc20-108">SearchStringParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="0dc20-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc20-109">DisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="0dc20-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc20-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="0dc20-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="0dc20-111">DESCRIPTION</span></span>
<span data-ttu-id="0dc20-112">Felsorolja a meglévő Azure Active Directory-alkalmazásokat.</span><span class="sxs-lookup"><span data-stu-id="0dc20-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="0dc20-113">Az alkalmazások keresése a ObjectId, az ApplicationId, a IdentifierUri vagy a DisplayName segítségével végezhető el.</span><span class="sxs-lookup"><span data-stu-id="0dc20-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="0dc20-114">Ha nincs megadva paraméter, a program az összes alkalmazást beolvassa a bérlői webhelyre.</span><span class="sxs-lookup"><span data-stu-id="0dc20-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="0dc20-115">Példák</span><span class="sxs-lookup"><span data-stu-id="0dc20-115">EXAMPLES</span></span>

### <span data-ttu-id="0dc20-116">Példa 1 – az összes alkalmazás listázása</span><span class="sxs-lookup"><span data-stu-id="0dc20-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzureRmADApplication
```

<span data-ttu-id="0dc20-117">Felsorolja az összes alkalmazást bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="0dc20-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="0dc20-118">Példa 2 – a lapozást használó alkalmazások listázása</span><span class="sxs-lookup"><span data-stu-id="0dc20-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzureRmADApplication -First 100
```

<span data-ttu-id="0dc20-119">Felsorolja az első 100-alkalmazásokat bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="0dc20-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="0dc20-120">Példa: 3 – az alkalmazás beolvasása azonosító URI azonosítóval</span><span class="sxs-lookup"><span data-stu-id="0dc20-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="0dc20-121">A "" azonosítóval kapja meg az alkalmazást http://mySecretApp1 .</span><span class="sxs-lookup"><span data-stu-id="0dc20-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="0dc20-122">Példa 4 – alkalmazásobjektum-azonosító beszerzése</span><span class="sxs-lookup"><span data-stu-id="0dc20-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="0dc20-123">A ' 39e64ec6-569b-4030-8e1c-c3c519a05d69 ' azonosítójú objektummal kapja meg az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="0dc20-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="0dc20-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0dc20-124">PARAMETERS</span></span>

### <span data-ttu-id="0dc20-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0dc20-125">-ApplicationId</span></span>
<span data-ttu-id="0dc20-126">A lekérni kívánt alkalmazás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0dc20-126">The application id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc20-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc20-127">-DefaultProfile</span></span>
<span data-ttu-id="0dc20-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0dc20-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0dc20-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0dc20-129">-DisplayName</span></span>
<span data-ttu-id="0dc20-130">Az alkalmazás megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="0dc20-130">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc20-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="0dc20-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="0dc20-132">A megjelenítendő névvel kezdődő összes alkalmazás beolvasása</span><span class="sxs-lookup"><span data-stu-id="0dc20-132">Fetch all applications starting with the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc20-133">– Első</span><span class="sxs-lookup"><span data-stu-id="0dc20-133">-First</span></span>
<span data-ttu-id="0dc20-134">A visszaadni kívánt objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="0dc20-134">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc20-135">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="0dc20-135">-IdentifierUri</span></span>
<span data-ttu-id="0dc20-136">A beolvasni kívánt alkalmazás egyedi azonosítójának URI azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0dc20-136">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc20-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="0dc20-137">-IncludeTotalCount</span></span>
<span data-ttu-id="0dc20-138">Az adathalmaz objektumainak számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="0dc20-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="0dc20-139">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="0dc20-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="0dc20-140">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0dc20-140">-ObjectId</span></span>
<span data-ttu-id="0dc20-141">A beolvasni kívánt alkalmazás objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0dc20-141">The object id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc20-142">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="0dc20-142">-Skip</span></span>
<span data-ttu-id="0dc20-143">Figyelmen kívül hagyja az első N objektumokat, és a fennmaradó objektumokat kapja.</span><span class="sxs-lookup"><span data-stu-id="0dc20-143">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc20-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc20-144">CommonParameters</span></span>
<span data-ttu-id="0dc20-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0dc20-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc20-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dc20-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc20-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0dc20-147">INPUTS</span></span>

### <span data-ttu-id="0dc20-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="0dc20-148">System.Guid</span></span>

### <span data-ttu-id="0dc20-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0dc20-149">System.String</span></span>

## <span data-ttu-id="0dc20-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0dc20-150">OUTPUTS</span></span>

### <span data-ttu-id="0dc20-151">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="0dc20-151">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="0dc20-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0dc20-152">NOTES</span></span>

## <span data-ttu-id="0dc20-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0dc20-153">RELATED LINKS</span></span>

[<span data-ttu-id="0dc20-154">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="0dc20-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="0dc20-155">Új – AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="0dc20-155">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="0dc20-156">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="0dc20-156">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="0dc20-157">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="0dc20-157">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)



[<span data-ttu-id="0dc20-158">Új – AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="0dc20-158">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

