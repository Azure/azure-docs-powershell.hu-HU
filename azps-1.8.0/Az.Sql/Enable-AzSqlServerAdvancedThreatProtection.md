---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: aaaf417137bb1ec16150a2bf3d0ac88b64e70fae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669057"
---
# <span data-ttu-id="44784-101">Enable-AzSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="44784-101">Enable-AzSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="44784-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="44784-102">SYNOPSIS</span></span>
<span data-ttu-id="44784-103">Lehetővé teszi a speciális veszélyforrások védelmét a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="44784-103">Enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="44784-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="44784-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44784-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="44784-105">DESCRIPTION</span></span>
<span data-ttu-id="44784-106">Az **enable-AzSqlServerAdvancedThreatProtection** parancsmag lehetővé teszi a speciális veszélyforrások védelmét a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="44784-106">The **Enable-AzSqlServerAdvancedThreatProtection** cmdlet enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="44784-107">Példák</span><span class="sxs-lookup"><span data-stu-id="44784-107">EXAMPLES</span></span>

### <span data-ttu-id="44784-108">Példa 1 – a Server Advanced Threat Protection engedélyezése</span><span class="sxs-lookup"><span data-stu-id="44784-108">Example 1 - Enable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="44784-109">Példa 2 – a kiszolgáló speciális veszélyforrások elleni védelem engedélyezése a kiszolgálói erőforrásból</span><span class="sxs-lookup"><span data-stu-id="44784-109">Example 2 - Enable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="44784-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="44784-110">PARAMETERS</span></span>

### <span data-ttu-id="44784-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44784-111">-DefaultProfile</span></span>
<span data-ttu-id="44784-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44784-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44784-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44784-113">-InputObject</span></span>
<span data-ttu-id="44784-114">A speciális veszélyforrások elleni védelemre vonatkozó házirend-művelethez használt kiszolgálói objektum</span><span class="sxs-lookup"><span data-stu-id="44784-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="44784-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44784-115">-ResourceGroupName</span></span>
<span data-ttu-id="44784-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="44784-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="44784-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="44784-117">-ServerName</span></span>
<span data-ttu-id="44784-118">SQL-adatbázis kiszolgálójának neve</span><span class="sxs-lookup"><span data-stu-id="44784-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="44784-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="44784-119">-Confirm</span></span>
<span data-ttu-id="44784-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="44784-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44784-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44784-121">-WhatIf</span></span>
<span data-ttu-id="44784-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="44784-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44784-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="44784-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44784-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44784-124">CommonParameters</span></span>
<span data-ttu-id="44784-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="44784-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44784-126">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="44784-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44784-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="44784-127">INPUTS</span></span>

### <span data-ttu-id="44784-128">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="44784-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="44784-129">System. String</span><span class="sxs-lookup"><span data-stu-id="44784-129">System.String</span></span>

## <span data-ttu-id="44784-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44784-130">OUTPUTS</span></span>

### <span data-ttu-id="44784-131">Microsoft. Azure. Command. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="44784-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="44784-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="44784-132">NOTES</span></span>

## <span data-ttu-id="44784-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44784-133">RELATED LINKS</span></span>
