---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 5dd2c495fa80826f88f96901df7a02ad33bf8e4f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334734"
---
# <span data-ttu-id="5ac29-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="5ac29-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="5ac29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ac29-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac29-103">Letiltja a speciális adatbiztonságot a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="5ac29-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="5ac29-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5ac29-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ac29-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5ac29-105">DESCRIPTION</span></span>
<span data-ttu-id="5ac29-106">A **Disable-AzSqlServerAdvancedDataSecurity** parancsmag letiltja a speciális adatbiztonságot a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="5ac29-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="5ac29-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5ac29-107">EXAMPLES</span></span>

### <span data-ttu-id="5ac29-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="5ac29-108">Example 1</span></span>
### <span data-ttu-id="5ac29-109">2. példa: A kiszolgáló speciális adatbiztonságának letiltása</span><span class="sxs-lookup"><span data-stu-id="5ac29-109">Example 2: Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="5ac29-110">3. példa: A kiszolgáló speciális adatbiztonságának letiltása a kiszolgálóerőforrásból</span><span class="sxs-lookup"><span data-stu-id="5ac29-110">Example 3: Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="5ac29-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ac29-111">PARAMETERS</span></span>

### <span data-ttu-id="5ac29-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac29-112">-DefaultProfile</span></span>
<span data-ttu-id="5ac29-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ac29-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ac29-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ac29-114">-InputObject</span></span>
<span data-ttu-id="5ac29-115">The server object to use with Advanced Data Security policy operation</span><span class="sxs-lookup"><span data-stu-id="5ac29-115">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="5ac29-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ac29-116">-ResourceGroupName</span></span>
<span data-ttu-id="5ac29-117">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5ac29-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="5ac29-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5ac29-118">-ServerName</span></span>
<span data-ttu-id="5ac29-119">SQL-adatbázis-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="5ac29-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="5ac29-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ac29-120">-Confirm</span></span>
<span data-ttu-id="5ac29-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5ac29-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ac29-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ac29-122">-WhatIf</span></span>
<span data-ttu-id="5ac29-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5ac29-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ac29-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ac29-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ac29-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac29-125">CommonParameters</span></span>
<span data-ttu-id="5ac29-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ac29-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac29-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ac29-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac29-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ac29-128">INPUTS</span></span>

### <span data-ttu-id="5ac29-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="5ac29-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="5ac29-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5ac29-130">System.String</span></span>

## <span data-ttu-id="5ac29-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ac29-131">OUTPUTS</span></span>

### <span data-ttu-id="5ac29-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5ac29-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="5ac29-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5ac29-133">NOTES</span></span>

## <span data-ttu-id="5ac29-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ac29-134">RELATED LINKS</span></span>
