---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
ms.openlocfilehash: 582b512ef502e0dac3fc443807f1e33a65063728
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186709"
---
# <span data-ttu-id="62707-101">Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="62707-101">Get-AzSqlCapability</span></span>

## <span data-ttu-id="62707-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62707-102">SYNOPSIS</span></span>
<span data-ttu-id="62707-103">Az SQL-adatbázis funkciói az aktuális előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="62707-103">Gets SQL Database capabilities for the current subscription.</span></span>

## <span data-ttu-id="62707-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62707-104">SYNTAX</span></span>

### <span data-ttu-id="62707-105">FilterResults (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="62707-105">FilterResults (Default)</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="62707-106">DefaultResults</span><span class="sxs-lookup"><span data-stu-id="62707-106">DefaultResults</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62707-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="62707-107">DESCRIPTION</span></span>
<span data-ttu-id="62707-108">A **Get-AzSqlCapability** parancsmag az Azure SQL-adatbázis elérhető funkcióit kapja meg a jelenlegi előfizetésben egy régióban.</span><span class="sxs-lookup"><span data-stu-id="62707-108">The **Get-AzSqlCapability** cmdlet gets the Azure SQL Database capabilities available on the current subscription for a region.</span></span>
<span data-ttu-id="62707-109">Ha megadja a *ServerVersionName* , a *EditionName* vagy a *ServiceObjectiveName* paramétert, ez a parancsmag a megadott értékeket és a megelőzőket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="62707-109">If you specify the *ServerVersionName* , *EditionName* , or *ServiceObjectiveName* parameters, this cmdlet returns the specified values and their predecessors.</span></span>

## <span data-ttu-id="62707-110">Példák</span><span class="sxs-lookup"><span data-stu-id="62707-110">EXAMPLES</span></span>

### <span data-ttu-id="62707-111">Példa 1: a meglévő előfizetéshez tartozó funkciók beszerzése egy adott régióban</span><span class="sxs-lookup"><span data-stu-id="62707-111">Example 1: Get capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

<span data-ttu-id="62707-112">Ez a parancs a közép-amerikai régió aktuális előfizetésének SQL-adatbázis-példányait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="62707-112">This command returns the capabilities for SQL Database instances on the current subscription for the Central US region.</span></span>

### <span data-ttu-id="62707-113">2. példa: a jelenlegi előfizetéshez tartozó alapértelmezett funkciók beszerzése egy régióban</span><span class="sxs-lookup"><span data-stu-id="62707-113">Example 2: Get default capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

<span data-ttu-id="62707-114">Ez a parancs a közép-amerikai régió jelenlegi előfizetésének alapértelmezett funkcióit számítja ki az SQL-adatbázisokban.</span><span class="sxs-lookup"><span data-stu-id="62707-114">This command returns the default capabilities for SQL Databases on the current subscription in the Central US region.</span></span>

### <span data-ttu-id="62707-115">3. példa: a szolgáltatási cél részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="62707-115">Example 3: Get details for a service objective</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

<span data-ttu-id="62707-116">Ez a parancs a jelenlegi előfizetéshez megadott szolgáltatási célhoz tartozó alapértelmezett funkciókat kapja meg az SQL-adatbázisokban.</span><span class="sxs-lookup"><span data-stu-id="62707-116">This command gets default capabilities for SQL Databases for the specified service objective on the current subscription.</span></span>

## <span data-ttu-id="62707-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62707-117">PARAMETERS</span></span>

### <span data-ttu-id="62707-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62707-118">-DefaultProfile</span></span>
<span data-ttu-id="62707-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="62707-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62707-120">– Alapértelmezett beállítások</span><span class="sxs-lookup"><span data-stu-id="62707-120">-Defaults</span></span>
<span data-ttu-id="62707-121">Azt jelzi, hogy ez a parancsmag csak alapértelmezés szerint válik elérhetővé.</span><span class="sxs-lookup"><span data-stu-id="62707-121">Indicates that this cmdlet gets only defaults.</span></span>

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

### <span data-ttu-id="62707-122">-EditionName</span><span class="sxs-lookup"><span data-stu-id="62707-122">-EditionName</span></span>
<span data-ttu-id="62707-123">Annak az adatbázis-kiadásnak a nevét adja meg, amelynek a parancsmagja elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="62707-123">Specifies the name of the database edition for which this cmdlet gets capabilities.</span></span>

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

### <span data-ttu-id="62707-124">-LocationName</span><span class="sxs-lookup"><span data-stu-id="62707-124">-LocationName</span></span>
<span data-ttu-id="62707-125">Annak a helynek a nevét adja meg, amelyre a parancsmag lehetőségeket ad.</span><span class="sxs-lookup"><span data-stu-id="62707-125">Specifies the name of the Location for which this cmdlet gets capabilities.</span></span>
<span data-ttu-id="62707-126">További információ: Azure Regions http://azure.microsoft.com/en-us/regions/ ( http://azure.microsoft.com/en-us/regions/) .</span><span class="sxs-lookup"><span data-stu-id="62707-126">For more information, see Azure Regionshttp://azure.microsoft.com/en-us/regions/ (http://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="62707-127">-ServerVersionName</span><span class="sxs-lookup"><span data-stu-id="62707-127">-ServerVersionName</span></span>
<span data-ttu-id="62707-128">Annak a kiszolgálói verziónak a nevét adja meg, amelynek a parancsmagja elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="62707-128">Specifies the name of the server version for which this cmdlet gets capabilities.</span></span>

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

### <span data-ttu-id="62707-129">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="62707-129">-ServiceObjectiveName</span></span>
<span data-ttu-id="62707-130">Annak a szolgáltatási célnak a nevét adja meg, amelyre ez a parancsmag lehetőségeket kap.</span><span class="sxs-lookup"><span data-stu-id="62707-130">Specifies the name of the service objective for which this cmdlet gets capabilities.</span></span>

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

### <span data-ttu-id="62707-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="62707-131">-Confirm</span></span>
<span data-ttu-id="62707-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="62707-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62707-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62707-133">-WhatIf</span></span>
<span data-ttu-id="62707-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="62707-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62707-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="62707-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62707-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62707-136">CommonParameters</span></span>
<span data-ttu-id="62707-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62707-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62707-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="62707-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62707-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62707-139">INPUTS</span></span>

### <span data-ttu-id="62707-140">System. String</span><span class="sxs-lookup"><span data-stu-id="62707-140">System.String</span></span>

## <span data-ttu-id="62707-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62707-141">OUTPUTS</span></span>

### <span data-ttu-id="62707-142">Microsoft.Azure.Commands.Sql.Location_Capabilities. Model. LocationCapabilityModel</span><span class="sxs-lookup"><span data-stu-id="62707-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span></span>

## <span data-ttu-id="62707-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62707-143">NOTES</span></span>

## <span data-ttu-id="62707-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62707-144">RELATED LINKS</span></span>
