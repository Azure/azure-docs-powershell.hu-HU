---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: ba169c54d2b4664473a0013be52e2d078827dcb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495728"
---
# <span data-ttu-id="15c14-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="15c14-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="15c14-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15c14-102">SYNOPSIS</span></span>
<span data-ttu-id="15c14-103">Beolvassa az alkalmazáshoz társított hitelesítő adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="15c14-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15c14-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15c14-104">SYNTAX</span></span>

### <span data-ttu-id="15c14-105">ApplicationObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15c14-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15c14-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15c14-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15c14-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="15c14-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15c14-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15c14-108">ApplicationObjectParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15c14-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="15c14-109">DESCRIPTION</span></span>
<span data-ttu-id="15c14-110">Az Get-AzureRmADAppCredential parancsmag használatával lekérheti az alkalmazáshoz társított hitelesítő adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="15c14-110">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="15c14-111">Ez a parancs az alkalmazáshoz társított összes hitelesítőadat-tulajdonságot (de nem a hitelesítő adatokat) fogja kikeresni.</span><span class="sxs-lookup"><span data-stu-id="15c14-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="15c14-112">Példák</span><span class="sxs-lookup"><span data-stu-id="15c14-112">EXAMPLES</span></span>

### <span data-ttu-id="15c14-113">Példa 1 – alkalmazásspecifikus hitelesítő adatok beszerzése objektum-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="15c14-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="15c14-114">A "1f99cf81-0146-4f4e-beae-2007d0668476" azonosítójú objektummal társított hitelesítő adatok listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="15c14-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="15c14-115">2 példa – az alkalmazás hitelesítő adatainak beolvasása csővezetéken</span><span class="sxs-lookup"><span data-stu-id="15c14-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzureRmADAppCredential
```

<span data-ttu-id="15c14-116">Beilleszti az alkalmazást a "1f99cf81-0146-4f4e-beae-2007d0668476" azonosítójú objektumazonosítót, és a Get-AzureRmADAppCredential parancsmaghoz illeszti az adott alkalmazás összes hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="15c14-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzureRmADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="15c14-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15c14-117">PARAMETERS</span></span>

### <span data-ttu-id="15c14-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="15c14-118">-ApplicationId</span></span>
<span data-ttu-id="15c14-119">Az alkalmazás azonosítója a hitelesítő adatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="15c14-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="15c14-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="15c14-120">-ApplicationObject</span></span>
<span data-ttu-id="15c14-121">Az Application objektum a hitelesítő adatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="15c14-121">The application object to retrieve credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15c14-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c14-122">-DefaultProfile</span></span>
<span data-ttu-id="15c14-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="15c14-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15c14-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="15c14-124">-DisplayName</span></span>
<span data-ttu-id="15c14-125">Az alkalmazás megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="15c14-125">The display name of the application.</span></span>

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

### <span data-ttu-id="15c14-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="15c14-126">-ObjectId</span></span>
<span data-ttu-id="15c14-127">A hitelesítő adatok beolvasására szolgáló alkalmazás objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="15c14-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="15c14-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c14-128">CommonParameters</span></span>
<span data-ttu-id="15c14-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15c14-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c14-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15c14-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c14-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15c14-131">INPUTS</span></span>

### <span data-ttu-id="15c14-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="15c14-132">System.Guid</span></span>

### <span data-ttu-id="15c14-133">System. String</span><span class="sxs-lookup"><span data-stu-id="15c14-133">System.String</span></span>

### <span data-ttu-id="15c14-134">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="15c14-134">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="15c14-135">Paraméterek: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="15c14-135">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="15c14-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15c14-136">OUTPUTS</span></span>

### <span data-ttu-id="15c14-137">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="15c14-137">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="15c14-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15c14-138">NOTES</span></span>

## <span data-ttu-id="15c14-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15c14-139">RELATED LINKS</span></span>

[<span data-ttu-id="15c14-140">Új – AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="15c14-140">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="15c14-141">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="15c14-141">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="15c14-142">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="15c14-142">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

