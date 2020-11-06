---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 686785F8-2085-4705-A74D-12B18A87E187
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 567cb47599a23bf83581afb97a425902ee0e159a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494318"
---
# <span data-ttu-id="15550-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="15550-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="15550-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15550-102">SYNOPSIS</span></span>
<span data-ttu-id="15550-103">A kiszolgáló hosszú távú adatmegőrzési boltozatát kapja.</span><span class="sxs-lookup"><span data-stu-id="15550-103">Gets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15550-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15550-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerBackupLongTermRetentionVault [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15550-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="15550-105">DESCRIPTION</span></span>
<span data-ttu-id="15550-106">A **Get-AzureRmSqlServerBackupLongTermRetentionVault** parancsmag a kiszolgálóhoz regisztrált hosszú távú adatmegőrzési boltozatot kapja.</span><span class="sxs-lookup"><span data-stu-id="15550-106">The **Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet gets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="15550-107">A boltozat a biztonsági másolatok adatainak tárolására szolgáló Azure Backup-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="15550-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="15550-108">Példák</span><span class="sxs-lookup"><span data-stu-id="15550-108">EXAMPLES</span></span>

## <span data-ttu-id="15550-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15550-109">PARAMETERS</span></span>

### <span data-ttu-id="15550-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15550-110">-DefaultProfile</span></span>
<span data-ttu-id="15550-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="15550-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15550-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15550-112">-ResourceGroupName</span></span>
<span data-ttu-id="15550-113">A kiszolgálót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="15550-113">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="15550-114">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="15550-114">-ServerName</span></span>
<span data-ttu-id="15550-115">Azt a kiszolgálót adja meg, amelynek a parancsmagja a boltozatot kapja.</span><span class="sxs-lookup"><span data-stu-id="15550-115">Specifies the server for which this cmdlet gets a vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15550-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="15550-116">-Confirm</span></span>
<span data-ttu-id="15550-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="15550-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15550-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15550-118">-WhatIf</span></span>
<span data-ttu-id="15550-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="15550-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15550-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="15550-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15550-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15550-121">CommonParameters</span></span>
<span data-ttu-id="15550-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15550-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15550-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15550-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15550-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15550-124">INPUTS</span></span>

### <span data-ttu-id="15550-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="15550-125">None</span></span>
<span data-ttu-id="15550-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="15550-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="15550-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15550-127">OUTPUTS</span></span>

## <span data-ttu-id="15550-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15550-128">NOTES</span></span>

## <span data-ttu-id="15550-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15550-129">RELATED LINKS</span></span>

[<span data-ttu-id="15550-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="15550-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Set-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="15550-131">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="15550-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

