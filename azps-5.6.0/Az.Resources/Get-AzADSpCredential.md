---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: 83212224ba14e0a079db936d058522d4759430fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923465"
---
# <span data-ttu-id="fd441-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="fd441-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="fd441-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd441-102">SYNOPSIS</span></span>
<span data-ttu-id="fd441-103">Beolvassa a szolgáltatásnévvel társított hitelesítő adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="fd441-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="fd441-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fd441-104">SYNTAX</span></span>

### <span data-ttu-id="fd441-105">ObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd441-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd441-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd441-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fd441-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd441-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd441-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd441-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd441-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fd441-109">DESCRIPTION</span></span>
<span data-ttu-id="fd441-110">A Get-AzADSpCredential parancsmaggal lekérheti a szolgáltatásnévvel társított hitelesítő adatok listáját.</span><span class="sxs-lookup"><span data-stu-id="fd441-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="fd441-111">Ez a parancs beolvassa a szolgáltatásnévvel társított összes hitelesítőadat-tulajdonságot (de a hitelesítő adatokat nem).</span><span class="sxs-lookup"><span data-stu-id="fd441-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="fd441-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fd441-112">EXAMPLES</span></span>

### <span data-ttu-id="fd441-113">1. példa : Hitelesítő adatok felsorolása SPN szerint</span><span class="sxs-lookup"><span data-stu-id="fd441-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="fd441-114">Visszaadja az egyszerű szolgáltatásnévvel (SPN) társított hitelesítő adatok http://test12345 listáját.</span><span class="sxs-lookup"><span data-stu-id="fd441-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="fd441-115">2. példa: A hitelesítő adatok listába sorolása objektumazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="fd441-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="fd441-116">A "58e28616-99cc-4da4-b705-7672130e1047" objektumazonosítóval társított egyszerű szolgáltatáshoz tartozó hitelesítő adatok listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="fd441-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="fd441-117">3. példa : A hitelesítő adatok felsorolása pipázás használatával</span><span class="sxs-lookup"><span data-stu-id="fd441-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="fd441-118">A "58e28616-99cc-4da4-b705-7672130e1047" objektumazonosítóval beszerzúdő egyszerű szolgáltatásnév, és a Get-AzADSpCredential-parancsmagba való betekintve felsorolja az adott egyszerű szolgáltatásnévhez szükséges összes hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="fd441-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="fd441-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd441-119">PARAMETERS</span></span>

### <span data-ttu-id="fd441-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd441-120">-DefaultProfile</span></span>
<span data-ttu-id="fd441-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fd441-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd441-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fd441-122">-DisplayName</span></span>
<span data-ttu-id="fd441-123">A szolgáltatásnév megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="fd441-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="fd441-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fd441-124">-ObjectId</span></span>
<span data-ttu-id="fd441-125">A szolgáltatásnév objektumazonosítója, amelyből a hitelesítő adatokat lekéri.</span><span class="sxs-lookup"><span data-stu-id="fd441-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd441-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fd441-126">-ServicePrincipalName</span></span>
<span data-ttu-id="fd441-127">A szolgáltatásnév (SPN) neve, amelyből a hitelesítő adatokat beolvassa.</span><span class="sxs-lookup"><span data-stu-id="fd441-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd441-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="fd441-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="fd441-129">A hitelesítő adatok beolvasására használt egyszerű szolgáltatásobjektum.</span><span class="sxs-lookup"><span data-stu-id="fd441-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd441-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd441-130">CommonParameters</span></span>
<span data-ttu-id="fd441-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd441-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd441-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd441-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd441-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd441-133">INPUTS</span></span>

### <span data-ttu-id="fd441-134">System.String</span><span class="sxs-lookup"><span data-stu-id="fd441-134">System.String</span></span>

### <span data-ttu-id="fd441-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="fd441-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="fd441-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd441-136">OUTPUTS</span></span>

### <span data-ttu-id="fd441-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="fd441-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="fd441-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fd441-138">NOTES</span></span>

## <span data-ttu-id="fd441-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd441-139">RELATED LINKS</span></span>

[<span data-ttu-id="fd441-140">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="fd441-140">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="fd441-141">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="fd441-141">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="fd441-142">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="fd441-142">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

