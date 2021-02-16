---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: ae92a4fa28f0715c7a2517f062113afb01a359cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144130"
---
# <span data-ttu-id="3f9e7-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="3f9e7-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="3f9e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f9e7-102">SYNOPSIS</span></span>
<span data-ttu-id="3f9e7-103">Feladatátvétel egy Azure SQL Felügyelt példányban.</span><span class="sxs-lookup"><span data-stu-id="3f9e7-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="3f9e7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3f9e7-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f9e7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3f9e7-105">DESCRIPTION</span></span>
<span data-ttu-id="3f9e7-106">Az **Invoke-AzSqlInstanceFailover** parancsmag feladatátvételt ad az Azure SQL Felügyelt példányhoz.</span><span class="sxs-lookup"><span data-stu-id="3f9e7-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="3f9e7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3f9e7-107">EXAMPLES</span></span>

### <span data-ttu-id="3f9e7-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="3f9e7-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="3f9e7-109">Ez a parancs feladatátvételt ad a "ManagedInstance01" nevű példány elsődleges példányának.</span><span class="sxs-lookup"><span data-stu-id="3f9e7-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="3f9e7-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="3f9e7-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="3f9e7-111">Ez a parancs feladatátvételt ad a felügyelt példány "ManagedInstance01" olvasható másodlagos példányának.</span><span class="sxs-lookup"><span data-stu-id="3f9e7-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="3f9e7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f9e7-112">PARAMETERS</span></span>

### <span data-ttu-id="3f9e7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f9e7-113">-AsJob</span></span>
<span data-ttu-id="3f9e7-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3f9e7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f9e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f9e7-115">-DefaultProfile</span></span>
<span data-ttu-id="3f9e7-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f9e7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f9e7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3f9e7-117">-Force</span></span>
<span data-ttu-id="3f9e7-118">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="3f9e7-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="3f9e7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3f9e7-119">-Name</span></span>
<span data-ttu-id="3f9e7-120">Az eltávolítható Azure SQL-példány neve.</span><span class="sxs-lookup"><span data-stu-id="3f9e7-120">The name of the Azure SQL instance to remove.</span></span>

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

### <span data-ttu-id="3f9e7-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f9e7-121">-PassThru</span></span>
<span data-ttu-id="3f9e7-122">Sikeres végrehajtás esetén igaz értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="3f9e7-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="3f9e7-123">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="3f9e7-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3f9e7-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="3f9e7-124">-ReadableSecondary</span></span>
<span data-ttu-id="3f9e7-125">Az alapértelmezett elsődleges replika helyett az olvasható másodlagos replika feladatátvétele</span><span class="sxs-lookup"><span data-stu-id="3f9e7-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="3f9e7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f9e7-126">-ResourceGroupName</span></span>
<span data-ttu-id="3f9e7-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3f9e7-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="3f9e7-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f9e7-128">-Confirm</span></span>
<span data-ttu-id="3f9e7-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3f9e7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f9e7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f9e7-130">-WhatIf</span></span>
<span data-ttu-id="3f9e7-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3f9e7-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f9e7-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f9e7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f9e7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f9e7-133">CommonParameters</span></span>
<span data-ttu-id="3f9e7-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f9e7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f9e7-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f9e7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f9e7-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f9e7-136">INPUTS</span></span>

### <span data-ttu-id="3f9e7-137">System.String</span><span class="sxs-lookup"><span data-stu-id="3f9e7-137">System.String</span></span>

## <span data-ttu-id="3f9e7-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f9e7-138">OUTPUTS</span></span>

## <span data-ttu-id="3f9e7-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3f9e7-139">NOTES</span></span>

## <span data-ttu-id="3f9e7-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f9e7-140">RELATED LINKS</span></span>
