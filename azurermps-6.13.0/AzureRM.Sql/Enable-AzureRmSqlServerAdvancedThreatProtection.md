---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/enable-azurermsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Enable-AzureRmSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Enable-AzureRmSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: 1276ba100a795ca113f1f09064bc46dfdfddf39b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679823"
---
# <span data-ttu-id="509e5-101">Enable-AzureRmSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="509e5-101">Enable-AzureRmSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="509e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="509e5-102">SYNOPSIS</span></span>
<span data-ttu-id="509e5-103">Lehetővé teszi a speciális veszélyforrások védelmét a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="509e5-103">Enables Advanced Threat Protection on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="509e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="509e5-104">SYNTAX</span></span>

```
Enable-AzureRmSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="509e5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="509e5-105">DESCRIPTION</span></span>
<span data-ttu-id="509e5-106">Az **enable-AzureRmSqlServerAdvancedThreatProtection** parancsmag lehetővé teszi a speciális veszélyforrások védelmét a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="509e5-106">The **Enable-AzureRmSqlServerAdvancedThreatProtection** cmdlet enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="509e5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="509e5-107">EXAMPLES</span></span>

### <span data-ttu-id="509e5-108">Példa 1 – a Server Advanced Threat Protection engedélyezése</span><span class="sxs-lookup"><span data-stu-id="509e5-108">Example 1 - Enable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Enable-AzureRmSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="509e5-109">Példa 2 – a kiszolgáló speciális veszélyforrások elleni védelem engedélyezése a kiszolgálói erőforrásból</span><span class="sxs-lookup"><span data-stu-id="509e5-109">Example 2 - Enable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzureRmSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="509e5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="509e5-110">PARAMETERS</span></span>

### <span data-ttu-id="509e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="509e5-111">-DefaultProfile</span></span>
<span data-ttu-id="509e5-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="509e5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509e5-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="509e5-113">-InputObject</span></span>
<span data-ttu-id="509e5-114">A speciális veszélyforrások elleni védelemre vonatkozó házirend-művelethez használt kiszolgálói objektum</span><span class="sxs-lookup"><span data-stu-id="509e5-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="509e5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="509e5-115">-ResourceGroupName</span></span>
<span data-ttu-id="509e5-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="509e5-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="509e5-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="509e5-117">-ServerName</span></span>
<span data-ttu-id="509e5-118">SQL-adatbázis kiszolgálójának neve</span><span class="sxs-lookup"><span data-stu-id="509e5-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="509e5-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="509e5-119">-Confirm</span></span>
<span data-ttu-id="509e5-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="509e5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="509e5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="509e5-121">-WhatIf</span></span>
<span data-ttu-id="509e5-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="509e5-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="509e5-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="509e5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="509e5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="509e5-124">CommonParameters</span></span>
<span data-ttu-id="509e5-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="509e5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="509e5-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="509e5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="509e5-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="509e5-127">INPUTS</span></span>

### <span data-ttu-id="509e5-128">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="509e5-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="509e5-129">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="509e5-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="509e5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="509e5-130">System.String</span></span>

## <span data-ttu-id="509e5-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="509e5-131">OUTPUTS</span></span>

### <span data-ttu-id="509e5-132">Microsoft. Azure. Command. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="509e5-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="509e5-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="509e5-133">NOTES</span></span>

## <span data-ttu-id="509e5-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="509e5-134">RELATED LINKS</span></span>
