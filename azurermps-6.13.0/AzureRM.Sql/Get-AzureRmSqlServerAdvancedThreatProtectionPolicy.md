---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveradvancedthreatprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.md
ms.openlocfilehash: 16762b56995b90422c78ad6dc5dd87461c0a8317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499359"
---
# <span data-ttu-id="56e1e-101">Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="56e1e-101">Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>

## <span data-ttu-id="56e1e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="56e1e-102">SYNOPSIS</span></span>
<span data-ttu-id="56e1e-103">Speciális veszélyforrások elleni védelemre vonatkozó házirendet kap a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="56e1e-103">Gets Advanced Threat Protection policy of a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56e1e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="56e1e-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAdvancedThreatProtectionPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56e1e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="56e1e-105">DESCRIPTION</span></span>
<span data-ttu-id="56e1e-106">A **Get-AzureRmSqlServerAdvancedThreatProtectionPolicy** parancsmag a kiszolgáló speciális veszélyforrásokkal kapcsolatos védelmi házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="56e1e-106">The **Get-AzureRmSqlServerAdvancedThreatProtectionPolicy** cmdlet retrives the Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="56e1e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="56e1e-107">EXAMPLES</span></span>

### <span data-ttu-id="56e1e-108">Példa 1 – a Server Advanced Threat Protectiont kapja</span><span class="sxs-lookup"><span data-stu-id="56e1e-108">Example 1 - Gets server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServerAdvancedThreatProtectionPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="56e1e-109">Példa: a Server Advanced Threat Protection a kiszolgálói erőforrásból</span><span class="sxs-lookup"><span data-stu-id="56e1e-109">Example 2 - Gets server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzureRmSqlServerAdvancedThreatProtectionPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="56e1e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="56e1e-110">PARAMETERS</span></span>

### <span data-ttu-id="56e1e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e1e-111">-DefaultProfile</span></span>
<span data-ttu-id="56e1e-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="56e1e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56e1e-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56e1e-113">-InputObject</span></span>
<span data-ttu-id="56e1e-114">A speciális veszélyforrások elleni védelemre vonatkozó házirend-művelethez használt kiszolgálói objektum</span><span class="sxs-lookup"><span data-stu-id="56e1e-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="56e1e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56e1e-115">-ResourceGroupName</span></span>
<span data-ttu-id="56e1e-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="56e1e-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="56e1e-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="56e1e-117">-ServerName</span></span>
<span data-ttu-id="56e1e-118">SQL-adatbázis kiszolgálójának neve</span><span class="sxs-lookup"><span data-stu-id="56e1e-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="56e1e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e1e-119">CommonParameters</span></span>
<span data-ttu-id="56e1e-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="56e1e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e1e-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56e1e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e1e-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="56e1e-122">INPUTS</span></span>

### <span data-ttu-id="56e1e-123">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="56e1e-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="56e1e-124">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="56e1e-124">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="56e1e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="56e1e-125">System.String</span></span>

## <span data-ttu-id="56e1e-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="56e1e-126">OUTPUTS</span></span>

### <span data-ttu-id="56e1e-127">Microsoft. Azure. Command. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="56e1e-127">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="56e1e-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="56e1e-128">NOTES</span></span>

## <span data-ttu-id="56e1e-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="56e1e-129">RELATED LINKS</span></span>
