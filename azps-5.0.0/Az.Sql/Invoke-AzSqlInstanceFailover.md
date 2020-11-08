---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: ae92a4fa28f0715c7a2517f062113afb01a359cf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185656"
---
# <span data-ttu-id="11021-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="11021-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="11021-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11021-102">SYNOPSIS</span></span>
<span data-ttu-id="11021-103">Azure SQL-alapú felügyelt példány feladatátvétele</span><span class="sxs-lookup"><span data-stu-id="11021-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="11021-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11021-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11021-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="11021-105">DESCRIPTION</span></span>
<span data-ttu-id="11021-106">A **meghívó-AzSqlInstanceFailover** parancsmag egy Azure SQL-alapú felügyelt példány feladatátvételét hajtja végre.</span><span class="sxs-lookup"><span data-stu-id="11021-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="11021-107">Példák</span><span class="sxs-lookup"><span data-stu-id="11021-107">EXAMPLES</span></span>

### <span data-ttu-id="11021-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="11021-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="11021-109">Ez a parancs a "ManagedInstance01" nevű példány elsődleges replikáját fogja lecserélni.</span><span class="sxs-lookup"><span data-stu-id="11021-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="11021-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="11021-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="11021-111">Ez a parancs a "ManagedInstance01" olvasható másodlagos replikát fogja átirányítani.</span><span class="sxs-lookup"><span data-stu-id="11021-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="11021-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11021-112">PARAMETERS</span></span>

### <span data-ttu-id="11021-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11021-113">-AsJob</span></span>
<span data-ttu-id="11021-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="11021-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11021-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11021-115">-DefaultProfile</span></span>
<span data-ttu-id="11021-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11021-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11021-117">-Force</span><span class="sxs-lookup"><span data-stu-id="11021-117">-Force</span></span>
<span data-ttu-id="11021-118">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="11021-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="11021-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="11021-119">-Name</span></span>
<span data-ttu-id="11021-120">Az eltávolítandó Azure SQL-példány neve.</span><span class="sxs-lookup"><span data-stu-id="11021-120">The name of the Azure SQL instance to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11021-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11021-121">-PassThru</span></span>
<span data-ttu-id="11021-122">Sikeres végrehajtás esetén az igaz értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="11021-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="11021-123">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="11021-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="11021-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="11021-124">-ReadableSecondary</span></span>
<span data-ttu-id="11021-125">Az olvasható másodlagos replika feladatátvétele az alapértelmezett elsődleges replika helyett</span><span class="sxs-lookup"><span data-stu-id="11021-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="11021-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11021-126">-ResourceGroupName</span></span>
<span data-ttu-id="11021-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="11021-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="11021-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="11021-128">-Confirm</span></span>
<span data-ttu-id="11021-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="11021-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11021-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11021-130">-WhatIf</span></span>
<span data-ttu-id="11021-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="11021-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11021-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11021-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11021-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11021-133">CommonParameters</span></span>
<span data-ttu-id="11021-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11021-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11021-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="11021-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11021-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11021-136">INPUTS</span></span>

### <span data-ttu-id="11021-137">System. String</span><span class="sxs-lookup"><span data-stu-id="11021-137">System.String</span></span>

## <span data-ttu-id="11021-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11021-138">OUTPUTS</span></span>

## <span data-ttu-id="11021-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11021-139">NOTES</span></span>

## <span data-ttu-id="11021-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11021-140">RELATED LINKS</span></span>
