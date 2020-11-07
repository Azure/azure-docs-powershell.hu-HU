---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: d6a06c3f4c50e10522ed06e6b1cd4185c1ef6768
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669059"
---
# <span data-ttu-id="10239-101">Disable-AzSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="10239-101">Disable-AzSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="10239-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10239-102">SYNOPSIS</span></span>
<span data-ttu-id="10239-103">Letiltja a speciális veszélyforrások védelmét a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="10239-103">Disables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="10239-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10239-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10239-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="10239-105">DESCRIPTION</span></span>
<span data-ttu-id="10239-106">A **disable-AzSqlServerAdvancedThreatProtection** parancsmag letiltja a speciális veszélyforrások védelmét a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="10239-106">The **Disable-AzSqlServerAdvancedThreatProtection** cmdlet disables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="10239-107">Példák</span><span class="sxs-lookup"><span data-stu-id="10239-107">EXAMPLES</span></span>

### <span data-ttu-id="10239-108">Példa 1 – a Server Advanced Threat Protection letiltása</span><span class="sxs-lookup"><span data-stu-id="10239-108">Example 1 - Disable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="10239-109">Példa 2 – a Server Advanced Threat Protection letiltása a kiszolgálói erőforrásból</span><span class="sxs-lookup"><span data-stu-id="10239-109">Example 2 - Disable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="10239-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10239-110">PARAMETERS</span></span>

### <span data-ttu-id="10239-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10239-111">-DefaultProfile</span></span>
<span data-ttu-id="10239-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10239-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10239-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10239-113">-InputObject</span></span>
<span data-ttu-id="10239-114">A speciális veszélyforrások elleni védelemre vonatkozó házirend-művelethez használt kiszolgálói objektum</span><span class="sxs-lookup"><span data-stu-id="10239-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="10239-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10239-115">-ResourceGroupName</span></span>
<span data-ttu-id="10239-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="10239-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="10239-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="10239-117">-ServerName</span></span>
<span data-ttu-id="10239-118">SQL-adatbázis kiszolgálójának neve</span><span class="sxs-lookup"><span data-stu-id="10239-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="10239-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="10239-119">-Confirm</span></span>
<span data-ttu-id="10239-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="10239-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10239-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10239-121">-WhatIf</span></span>
<span data-ttu-id="10239-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="10239-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10239-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="10239-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10239-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10239-124">CommonParameters</span></span>
<span data-ttu-id="10239-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10239-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10239-126">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="10239-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10239-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10239-127">INPUTS</span></span>

### <span data-ttu-id="10239-128">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="10239-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="10239-129">System. String</span><span class="sxs-lookup"><span data-stu-id="10239-129">System.String</span></span>

## <span data-ttu-id="10239-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10239-130">OUTPUTS</span></span>

### <span data-ttu-id="10239-131">Microsoft. Azure. Command. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="10239-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="10239-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10239-132">NOTES</span></span>

## <span data-ttu-id="10239-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10239-133">RELATED LINKS</span></span>
