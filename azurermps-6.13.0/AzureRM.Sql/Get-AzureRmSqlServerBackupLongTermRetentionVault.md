---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 686785F8-2085-4705-A74D-12B18A87E187
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 0aeee8e991d0f74a341a750e69016b12027fe584
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497259"
---
# <span data-ttu-id="6eff4-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="6eff4-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="6eff4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6eff4-102">SYNOPSIS</span></span>
<span data-ttu-id="6eff4-103">A kiszolgáló hosszú távú adatmegőrzési boltozatát kapja.</span><span class="sxs-lookup"><span data-stu-id="6eff4-103">Gets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6eff4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6eff4-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerBackupLongTermRetentionVault [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eff4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6eff4-105">DESCRIPTION</span></span>
<span data-ttu-id="6eff4-106">A **Get-AzureRmSqlServerBackupLongTermRetentionVault** parancsmag a kiszolgálóhoz regisztrált hosszú távú adatmegőrzési boltozatot kapja.</span><span class="sxs-lookup"><span data-stu-id="6eff4-106">The **Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet gets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="6eff4-107">A boltozat a biztonsági másolatok adatainak tárolására szolgáló Azure Backup-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="6eff4-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="6eff4-108">Példák</span><span class="sxs-lookup"><span data-stu-id="6eff4-108">EXAMPLES</span></span>

## <span data-ttu-id="6eff4-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6eff4-109">PARAMETERS</span></span>

### <span data-ttu-id="6eff4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eff4-110">-DefaultProfile</span></span>
<span data-ttu-id="6eff4-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6eff4-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6eff4-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eff4-112">-ResourceGroupName</span></span>
<span data-ttu-id="6eff4-113">A kiszolgálót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6eff4-113">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="6eff4-114">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="6eff4-114">-ServerName</span></span>
<span data-ttu-id="6eff4-115">Azt a kiszolgálót adja meg, amelynek a parancsmagja a boltozatot kapja.</span><span class="sxs-lookup"><span data-stu-id="6eff4-115">Specifies the server for which this cmdlet gets a vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eff4-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6eff4-116">-Confirm</span></span>
<span data-ttu-id="6eff4-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6eff4-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eff4-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eff4-118">-WhatIf</span></span>
<span data-ttu-id="6eff4-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6eff4-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eff4-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6eff4-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eff4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eff4-121">CommonParameters</span></span>
<span data-ttu-id="6eff4-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6eff4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eff4-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eff4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eff4-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6eff4-124">INPUTS</span></span>

### <span data-ttu-id="6eff4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6eff4-125">System.String</span></span>

## <span data-ttu-id="6eff4-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6eff4-126">OUTPUTS</span></span>

### <span data-ttu-id="6eff4-127">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlServerBackupLongTermRetentionVaultModel</span><span class="sxs-lookup"><span data-stu-id="6eff4-127">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlServerBackupLongTermRetentionVaultModel</span></span>

## <span data-ttu-id="6eff4-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6eff4-128">NOTES</span></span>

## <span data-ttu-id="6eff4-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6eff4-129">RELATED LINKS</span></span>

[<span data-ttu-id="6eff4-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="6eff4-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Set-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="6eff4-131">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="6eff4-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

