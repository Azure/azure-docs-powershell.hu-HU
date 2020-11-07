---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvancedthreatprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionPolicy.md
ms.openlocfilehash: dce8018e97e01c10356e77d321d564690cc03f71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668956"
---
# <span data-ttu-id="7ede3-101">Get-AzSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7ede3-101">Get-AzSqlServerAdvancedThreatProtectionPolicy</span></span>

## <span data-ttu-id="7ede3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ede3-102">SYNOPSIS</span></span>
<span data-ttu-id="7ede3-103">Speciális veszélyforrások elleni védelemre vonatkozó házirendet kap a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="7ede3-103">Gets Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="7ede3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ede3-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ede3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ede3-105">DESCRIPTION</span></span>
<span data-ttu-id="7ede3-106">A **Get-AzSqlServerAdvancedThreatProtectionPolicy** parancsmag a kiszolgáló speciális veszélyforrásokkal kapcsolatos védelmi házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7ede3-106">The **Get-AzSqlServerAdvancedThreatProtectionPolicy** cmdlet retrives the Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="7ede3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7ede3-107">EXAMPLES</span></span>

### <span data-ttu-id="7ede3-108">Példa 1 – a Server Advanced Threat Protectiont kapja</span><span class="sxs-lookup"><span data-stu-id="7ede3-108">Example 1 - Gets server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedThreatProtectionPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="7ede3-109">Példa: a Server Advanced Threat Protection a kiszolgálói erőforrásból</span><span class="sxs-lookup"><span data-stu-id="7ede3-109">Example 2 - Gets server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedThreatProtectionPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="7ede3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ede3-110">PARAMETERS</span></span>

### <span data-ttu-id="7ede3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ede3-111">-DefaultProfile</span></span>
<span data-ttu-id="7ede3-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ede3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ede3-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ede3-113">-InputObject</span></span>
<span data-ttu-id="7ede3-114">A speciális veszélyforrások elleni védelemre vonatkozó házirend-művelethez használt kiszolgálói objektum</span><span class="sxs-lookup"><span data-stu-id="7ede3-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="7ede3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ede3-115">-ResourceGroupName</span></span>
<span data-ttu-id="7ede3-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7ede3-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="7ede3-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="7ede3-117">-ServerName</span></span>
<span data-ttu-id="7ede3-118">SQL-adatbázis kiszolgálójának neve</span><span class="sxs-lookup"><span data-stu-id="7ede3-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="7ede3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ede3-119">CommonParameters</span></span>
<span data-ttu-id="7ede3-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ede3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ede3-121">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7ede3-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ede3-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ede3-122">INPUTS</span></span>

### <span data-ttu-id="7ede3-123">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="7ede3-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="7ede3-124">System. String</span><span class="sxs-lookup"><span data-stu-id="7ede3-124">System.String</span></span>

## <span data-ttu-id="7ede3-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ede3-125">OUTPUTS</span></span>

### <span data-ttu-id="7ede3-126">Microsoft. Azure. Command. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="7ede3-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="7ede3-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ede3-127">NOTES</span></span>

## <span data-ttu-id="7ede3-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ede3-128">RELATED LINKS</span></span>
