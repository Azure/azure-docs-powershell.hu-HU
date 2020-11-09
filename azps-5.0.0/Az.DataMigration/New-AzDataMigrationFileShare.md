---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: c0b88b60127162d895eeb642269240b699836d4f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297650"
---
# <span data-ttu-id="fc454-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="fc454-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="fc454-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc454-102">SYNOPSIS</span></span>
<span data-ttu-id="fc454-103">Létrehozza az Azure adatbázis-áttelepítési szolgáltatás fájlmegosztásról objektumát, amely a helyi hálózati megosztást adja meg a forrás adatbázis biztonsági másolatának elkészítéséhez.</span><span class="sxs-lookup"><span data-stu-id="fc454-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="fc454-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc454-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc454-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc454-105">DESCRIPTION</span></span>
<span data-ttu-id="fc454-106">A New-AzDataMigrationFileShare parancsmag hozza létre a fájlmegosztásról objektumot, amely a helyi hálózati megosztást adja meg, amelyet az Azure adatbázis-áttelepítési szolgáltatás a forrás-adatbázis biztonsági másolatai készítéséhez használ</span><span class="sxs-lookup"><span data-stu-id="fc454-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="fc454-107">Az SQL Server-példányt futtató szolgáltatásfiók írási jogosultsággal kell rendelkeznie ebben a hálózati megosztásban.</span><span class="sxs-lookup"><span data-stu-id="fc454-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="fc454-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fc454-108">EXAMPLES</span></span>

### <span data-ttu-id="fc454-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fc454-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="fc454-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc454-110">PARAMETERS</span></span>

### <span data-ttu-id="fc454-111">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="fc454-111">-Credential</span></span>
<span data-ttu-id="fc454-112">Hitelesítő adatok a fájlmegosztás eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="fc454-112">Credentials to access the file share.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc454-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc454-113">-DefaultProfile</span></span>
<span data-ttu-id="fc454-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc454-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc454-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="fc454-115">-Path</span></span>
<span data-ttu-id="fc454-116">Fájlmegosztási elérési út.</span><span class="sxs-lookup"><span data-stu-id="fc454-116">File share path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc454-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc454-117">CommonParameters</span></span>
<span data-ttu-id="fc454-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc454-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc454-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc454-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc454-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc454-120">INPUTS</span></span>

### <span data-ttu-id="fc454-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="fc454-121">None</span></span>

## <span data-ttu-id="fc454-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc454-122">OUTPUTS</span></span>

### <span data-ttu-id="fc454-123">Microsoft. Azure. Management. DataMigration. models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="fc454-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="fc454-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc454-124">NOTES</span></span>

## <span data-ttu-id="fc454-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc454-125">RELATED LINKS</span></span>
