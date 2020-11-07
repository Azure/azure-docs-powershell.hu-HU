---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: c2c3b634eb5a9e031c375a6cc696298becd58e8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839072"
---
# <span data-ttu-id="8f6fa-101">Enable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="8f6fa-101">Enable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="8f6fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f6fa-102">SYNOPSIS</span></span>
<span data-ttu-id="8f6fa-103">Lehetővé teszi a speciális adatbiztonságot a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="8f6fa-103">Enables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="8f6fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f6fa-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f6fa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f6fa-105">DESCRIPTION</span></span>
<span data-ttu-id="8f6fa-106">Az **enable-AzSqlServerAdvancedDataSecurity** parancsmag lehetővé teszi a speciális adatbiztonságot a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="8f6fa-106">The **Enable-AzSqlServerAdvancedDataSecurity** cmdlet enables Advanced Data Security on a server.</span></span> <span data-ttu-id="8f6fa-107">Advanced Data Security egy egységes biztonsági csomag, amely magában foglalja az adatosztályozást, a sebezhetőségi felmérést és a komplex veszélyforrások védelmét a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="8f6fa-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your server.</span></span> <span data-ttu-id="8f6fa-108">(Új tárolási fiókot hoz létre a program automatikusan a sebezhetőségi felmérések mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="8f6fa-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="8f6fa-109">Ha korábban már létrehozott egy tárolási fiókot erre a célra, akkor a program Ehelyett ezt fogja használni.</span><span class="sxs-lookup"><span data-stu-id="8f6fa-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="8f6fa-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8f6fa-110">EXAMPLES</span></span>

### <span data-ttu-id="8f6fa-111">Példa 1 – a Server Advanced Data Security engedélyezése</span><span class="sxs-lookup"><span data-stu-id="8f6fa-111">Example 1 - Enable server Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="8f6fa-112">Példa 2 – a kiszolgáló speciális adatbiztonságának engedélyezése a kiszolgálói erőforrásból</span><span class="sxs-lookup"><span data-stu-id="8f6fa-112">Example 2 - Enable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="8f6fa-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f6fa-113">PARAMETERS</span></span>

### <span data-ttu-id="8f6fa-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f6fa-114">-AsJob</span></span>
<span data-ttu-id="8f6fa-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8f6fa-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f6fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f6fa-116">-DefaultProfile</span></span>
<span data-ttu-id="8f6fa-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f6fa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f6fa-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="8f6fa-118">-DeploymentName</span></span>
<span data-ttu-id="8f6fa-119">Adjon meg egy egyéni nevet a speciális adatbiztonság telepítéséhez</span><span class="sxs-lookup"><span data-stu-id="8f6fa-119">Supply a custom name for Advanced Data Security deployment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f6fa-120">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="8f6fa-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="8f6fa-121">Ne engedélyezze az automatikus biztonsági rések felmérését (ez nem hoz létre tárolási fiókot)</span><span class="sxs-lookup"><span data-stu-id="8f6fa-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="8f6fa-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f6fa-122">-InputObject</span></span>
<span data-ttu-id="8f6fa-123">A kiszolgálói objektum, amely a speciális adatbiztonsági házirend-művelethez van használatban</span><span class="sxs-lookup"><span data-stu-id="8f6fa-123">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f6fa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f6fa-124">-ResourceGroupName</span></span>
<span data-ttu-id="8f6fa-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8f6fa-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="8f6fa-126">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="8f6fa-126">-ServerName</span></span>
<span data-ttu-id="8f6fa-127">SQL-adatbázis kiszolgálójának neve</span><span class="sxs-lookup"><span data-stu-id="8f6fa-127">SQL Database server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f6fa-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8f6fa-128">-Confirm</span></span>
<span data-ttu-id="8f6fa-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8f6fa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f6fa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f6fa-130">-WhatIf</span></span>
<span data-ttu-id="8f6fa-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8f6fa-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f6fa-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f6fa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f6fa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f6fa-133">CommonParameters</span></span>
<span data-ttu-id="8f6fa-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f6fa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f6fa-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f6fa-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f6fa-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f6fa-136">INPUTS</span></span>

### <span data-ttu-id="8f6fa-137">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="8f6fa-137">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="8f6fa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8f6fa-138">System.String</span></span>

## <span data-ttu-id="8f6fa-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f6fa-139">OUTPUTS</span></span>

### <span data-ttu-id="8f6fa-140">Microsoft. Azure. Command. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="8f6fa-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="8f6fa-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f6fa-141">NOTES</span></span>

## <span data-ttu-id="8f6fa-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f6fa-142">RELATED LINKS</span></span>
