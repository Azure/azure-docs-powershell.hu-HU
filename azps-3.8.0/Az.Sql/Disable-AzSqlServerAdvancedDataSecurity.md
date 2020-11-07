---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 482a620552457993795ba03e2da9367df5efa614
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93844950"
---
# <span data-ttu-id="abd4e-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="abd4e-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="abd4e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abd4e-102">SYNOPSIS</span></span>
<span data-ttu-id="abd4e-103">Letiltja a kiszolgálón a speciális adatbiztonságot.</span><span class="sxs-lookup"><span data-stu-id="abd4e-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="abd4e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abd4e-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="abd4e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="abd4e-105">DESCRIPTION</span></span>
<span data-ttu-id="abd4e-106">A **disable-AzSqlServerAdvancedDataSecurity** parancsmag letiltja a kiszolgálón a speciális adatbiztonságot.</span><span class="sxs-lookup"><span data-stu-id="abd4e-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="abd4e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="abd4e-107">EXAMPLES</span></span>

### <span data-ttu-id="abd4e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="abd4e-108">Example 1</span></span>
### <span data-ttu-id="abd4e-109">Példa 1 – a Server Advanced Data Security letiltása</span><span class="sxs-lookup"><span data-stu-id="abd4e-109">Example 1 - Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="abd4e-110">Példa 2 – a Server Advanced Data Security letiltása a kiszolgálói erőforrásból</span><span class="sxs-lookup"><span data-stu-id="abd4e-110">Example 2 - Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="abd4e-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abd4e-111">PARAMETERS</span></span>

### <span data-ttu-id="abd4e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abd4e-112">-DefaultProfile</span></span>
<span data-ttu-id="abd4e-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="abd4e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abd4e-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abd4e-114">-InputObject</span></span>
<span data-ttu-id="abd4e-115">A kiszolgálói objektum, amely a speciális adatbiztonsági házirend-művelethez van használatban</span><span class="sxs-lookup"><span data-stu-id="abd4e-115">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="abd4e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abd4e-116">-ResourceGroupName</span></span>
<span data-ttu-id="abd4e-117">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="abd4e-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="abd4e-118">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="abd4e-118">-ServerName</span></span>
<span data-ttu-id="abd4e-119">SQL-adatbázis kiszolgálójának neve</span><span class="sxs-lookup"><span data-stu-id="abd4e-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="abd4e-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="abd4e-120">-Confirm</span></span>
<span data-ttu-id="abd4e-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="abd4e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abd4e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abd4e-122">-WhatIf</span></span>
<span data-ttu-id="abd4e-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="abd4e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abd4e-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="abd4e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abd4e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abd4e-125">CommonParameters</span></span>
<span data-ttu-id="abd4e-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abd4e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abd4e-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="abd4e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abd4e-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abd4e-128">INPUTS</span></span>

### <span data-ttu-id="abd4e-129">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="abd4e-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="abd4e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="abd4e-130">System.String</span></span>

## <span data-ttu-id="abd4e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abd4e-131">OUTPUTS</span></span>

### <span data-ttu-id="abd4e-132">Microsoft. Azure. Command. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="abd4e-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="abd4e-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abd4e-133">NOTES</span></span>

## <span data-ttu-id="abd4e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abd4e-134">RELATED LINKS</span></span>
