---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
ms.openlocfilehash: 582b512ef502e0dac3fc443807f1e33a65063728
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165003"
---
# <span data-ttu-id="c7037-101">Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="c7037-101">Get-AzSqlCapability</span></span>

## <span data-ttu-id="c7037-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7037-102">SYNOPSIS</span></span>
<span data-ttu-id="c7037-103">SQL-adatbázis-funkciókat kap az aktuális előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="c7037-103">Gets SQL Database capabilities for the current subscription.</span></span>

## <span data-ttu-id="c7037-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c7037-104">SYNTAX</span></span>

### <span data-ttu-id="c7037-105">FilterResults (Alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c7037-105">FilterResults (Default)</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7037-106">DefaultResults</span><span class="sxs-lookup"><span data-stu-id="c7037-106">DefaultResults</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7037-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c7037-107">DESCRIPTION</span></span>
<span data-ttu-id="c7037-108">A **Get-AzSqlCapability** parancsmag az Azure SQL-adatbázis funkcióit az aktuális előfizetésben elérhetővé válik egy adott régióhoz.</span><span class="sxs-lookup"><span data-stu-id="c7037-108">The **Get-AzSqlCapability** cmdlet gets the Azure SQL Database capabilities available on the current subscription for a region.</span></span>
<span data-ttu-id="c7037-109">Ha megadja a *ServerVersionName,* *a EditionName* vagy a *ServiceObjectiveName* paramétert, ez a parancsmag a megadott értékeket és azok megelőzőit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="c7037-109">If you specify the *ServerVersionName*, *EditionName*, or *ServiceObjectiveName* parameters, this cmdlet returns the specified values and their predecessors.</span></span>

## <span data-ttu-id="c7037-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c7037-110">EXAMPLES</span></span>

### <span data-ttu-id="c7037-111">1. példa: Képességek lekérte az aktuális előfizetést egy régióhoz</span><span class="sxs-lookup"><span data-stu-id="c7037-111">Example 1: Get capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

<span data-ttu-id="c7037-112">Ez a parancs a közép-amerikai régió aktuális előfizetésében lévő SQL-adatbázis-példányok képességeit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="c7037-112">This command returns the capabilities for SQL Database instances on the current subscription for the Central US region.</span></span>

### <span data-ttu-id="c7037-113">2. példa: Alapértelmezett funkciók lekérte az aktuális előfizetéshez egy régióhoz</span><span class="sxs-lookup"><span data-stu-id="c7037-113">Example 2: Get default capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

<span data-ttu-id="c7037-114">Ez a parancs a közép-amerikai régió aktuális előfizetésében lévő SQL-adatbázisok alapértelmezett funkcióit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="c7037-114">This command returns the default capabilities for SQL Databases on the current subscription in the Central US region.</span></span>

### <span data-ttu-id="c7037-115">3. példa: Szolgáltatás-célkitűzés részleteinek lekérte</span><span class="sxs-lookup"><span data-stu-id="c7037-115">Example 3: Get details for a service objective</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

<span data-ttu-id="c7037-116">Ez a parancs az SQL-adatbázisok alapértelmezett funkcióit kapja az aktuális előfizetés megadott szolgáltatási célértékéhez.</span><span class="sxs-lookup"><span data-stu-id="c7037-116">This command gets default capabilities for SQL Databases for the specified service objective on the current subscription.</span></span>

## <span data-ttu-id="c7037-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7037-117">PARAMETERS</span></span>

### <span data-ttu-id="c7037-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7037-118">-DefaultProfile</span></span>
<span data-ttu-id="c7037-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c7037-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7037-120">-Alapértékek</span><span class="sxs-lookup"><span data-stu-id="c7037-120">-Defaults</span></span>
<span data-ttu-id="c7037-121">Azt jelzi, hogy ez a parancsmag csak alapértékeket kap.</span><span class="sxs-lookup"><span data-stu-id="c7037-121">Indicates that this cmdlet gets only defaults.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7037-122">-EditionName</span><span class="sxs-lookup"><span data-stu-id="c7037-122">-EditionName</span></span>
<span data-ttu-id="c7037-123">Annak az adatbázis-kiadásnak a neve, amelyhez a parancsmag képességeket kap.</span><span class="sxs-lookup"><span data-stu-id="c7037-123">Specifies the name of the database edition for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7037-124">-LocationName</span><span class="sxs-lookup"><span data-stu-id="c7037-124">-LocationName</span></span>
<span data-ttu-id="c7037-125">Megadja annak a helynek a nevét, amelyhez a parancsmag képességeket kap.</span><span class="sxs-lookup"><span data-stu-id="c7037-125">Specifies the name of the Location for which this cmdlet gets capabilities.</span></span>
<span data-ttu-id="c7037-126">További információt az Azure Régiók http://azure.microsoft.com/en-us/regions/ ( . http://azure.microsoft.com/en-us/regions/)</span><span class="sxs-lookup"><span data-stu-id="c7037-126">For more information, see Azure Regionshttp://azure.microsoft.com/en-us/regions/ (http://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7037-127">-ServerVersionName</span><span class="sxs-lookup"><span data-stu-id="c7037-127">-ServerVersionName</span></span>
<span data-ttu-id="c7037-128">Annak a kiszolgálóverziónak a neve, amelyhez a parancsmag képességeket kap.</span><span class="sxs-lookup"><span data-stu-id="c7037-128">Specifies the name of the server version for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7037-129">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="c7037-129">-ServiceObjectiveName</span></span>
<span data-ttu-id="c7037-130">Annak a szolgáltatási célnak a nevét adja meg, amelyhez a parancsmag képességeket kap.</span><span class="sxs-lookup"><span data-stu-id="c7037-130">Specifies the name of the service objective for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7037-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7037-131">-Confirm</span></span>
<span data-ttu-id="c7037-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c7037-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7037-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7037-133">-WhatIf</span></span>
<span data-ttu-id="c7037-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c7037-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7037-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c7037-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7037-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7037-136">CommonParameters</span></span>
<span data-ttu-id="c7037-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7037-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7037-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7037-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7037-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7037-139">INPUTS</span></span>

### <span data-ttu-id="c7037-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c7037-140">System.String</span></span>

## <span data-ttu-id="c7037-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7037-141">OUTPUTS</span></span>

### <span data-ttu-id="c7037-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span><span class="sxs-lookup"><span data-stu-id="c7037-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span></span>

## <span data-ttu-id="c7037-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c7037-143">NOTES</span></span>

## <span data-ttu-id="c7037-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7037-144">RELATED LINKS</span></span>
