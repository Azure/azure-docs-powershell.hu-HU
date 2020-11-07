---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 74956ff74beeb166a7788d0e577a86a4d2538ded
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839183"
---
# <span data-ttu-id="b44de-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="b44de-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="b44de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b44de-102">SYNOPSIS</span></span>
<span data-ttu-id="b44de-103">Speciális adatbiztonsági házirendet kap egy kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="b44de-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="b44de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b44de-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b44de-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b44de-105">DESCRIPTION</span></span>
<span data-ttu-id="b44de-106">A **Get-AzSqlServerAdvancedDataSecurityPolicy** parancsmag a kiszolgáló speciális adatbiztonsági házirendjének lekérdezését kéri.</span><span class="sxs-lookup"><span data-stu-id="b44de-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="b44de-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b44de-107">EXAMPLES</span></span>

### <span data-ttu-id="b44de-108">Példa 1 – a kiszolgáló speciális adatbiztonsága</span><span class="sxs-lookup"><span data-stu-id="b44de-108">Example 1 - Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="b44de-109">Példa: a Server Advanced Data Security a kiszolgáló-erőforrástól kapja</span><span class="sxs-lookup"><span data-stu-id="b44de-109">Example 2 - Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="b44de-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b44de-110">PARAMETERS</span></span>

### <span data-ttu-id="b44de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b44de-111">-DefaultProfile</span></span>
<span data-ttu-id="b44de-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b44de-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b44de-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b44de-113">-InputObject</span></span>
<span data-ttu-id="b44de-114">A kiszolgálói objektum, amely a speciális adatbiztonsági házirend-művelethez van használatban</span><span class="sxs-lookup"><span data-stu-id="b44de-114">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b44de-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b44de-115">-ResourceGroupName</span></span>
<span data-ttu-id="b44de-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b44de-116">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b44de-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="b44de-117">-ServerName</span></span>
<span data-ttu-id="b44de-118">SQL-adatbázis kiszolgálójának neve</span><span class="sxs-lookup"><span data-stu-id="b44de-118">SQL Database server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b44de-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b44de-119">CommonParameters</span></span>
<span data-ttu-id="b44de-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b44de-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b44de-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b44de-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b44de-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b44de-122">INPUTS</span></span>

### <span data-ttu-id="b44de-123">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="b44de-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="b44de-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b44de-124">System.String</span></span>

## <span data-ttu-id="b44de-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b44de-125">OUTPUTS</span></span>

### <span data-ttu-id="b44de-126">Microsoft. Azure. Command. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b44de-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="b44de-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b44de-127">NOTES</span></span>

## <span data-ttu-id="b44de-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b44de-128">RELATED LINKS</span></span>
